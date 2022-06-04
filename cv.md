# **Pavlovets Alexander**
**********
## **Contact information**:

1. **Phone number:** +375259407181
2. **E-mail:** pavlovecccc@gmail alex.pavlovets@gmail.com 
3. **GitHub:** alex-pavlovecccc
4. **LinkedIn:** https://www.linkedin.com/in/alexander-pavlovets-476017178/
*****************

## **About Myself**:
****************


## **Skills**:

* HTML (basic)
* CSS (basic)
* Git
* Swift 
    + UIKit
    + AutoLayout
    + API
    + MVVM, MVC
    + CoreData, UserDefault, UIGestures
    + Delegate 
* OOP
* Xcode
****************

### ***Code example***:
```
class NetworkService {
    
    //MARK: - host
    private let baseHost = "https://itunes.apple.com/search?term="
    
    func getAllTrack(searchStr: String, complition: @escaping([Song], Error?) -> Void) {
        let rightStr = searchStr.replacingOccurrences(of: " ", with: "+")
        guard let url = URL(string: self.baseHost + "\(rightStr.lowercased())"+"&entity=musicTrack") else { return }
        var request = URLRequest(url: url)
        request.httpMethod = "POST"
        
        URLSession.shared.dataTask(with: request) { responseData, responseInfo, error in
            
            if let error = error {
                print(error.localizedDescription)
            } else if let data = responseData {
                let object = try? JSONDecoder().decode(SearchResponse.self, from: data)
                DispatchQueue.main.async {
                    complition(object?.results ?? [], nil)
                }
            }
        }.resume()
    }
}
```
***************

## **Experience**:

****************

    
## **Education**:
1. Music College named after М.I GLINKA
2. Belarusian-Russian University faculty of Distance Learning

*****************
## **English**:
A2

