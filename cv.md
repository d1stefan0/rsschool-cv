1. Eugene Stefanovich
2. email: mejogi000@gmail.com, mobile/telegram: +375296690010
3. I would like to get some experience in a new programming language for me
4. Skills
- programming language - swift
- good knowledge main tools swift development such as Xcode, Storyboard, GitHub, BitBucket and others
- good knowledge main frameworks iOS SDK (Foundation, UIKit and others)
- knowledge CoreData, Realm, Alamofire and other
- knowledge main design patterns and principles of object oriented programming
- understanding the principles of work client-server and mobile applications 

5. Сurrently studying ARKit framework
```Swift
import SceneKit

class VirtualObject: SCNReferenceNode {
    
    static let availableObjects: [SCNReferenceNode] = {
        
        guard let modelsURLs = Bundle.main.url(forResource: "art.scnassets", withExtension: nil) else { return [] }
        
        let fileEnumirator = FileManager().enumerator(at: modelsURLs, includingPropertiesForKeys: nil)!
        
        return fileEnumirator.compactMap{ element in
            let url = element as! URL
            
            guard url.pathExtension == "scn" else { return nil }
            
            return VirtualObject(url: url)
        }
    }()
}
```
6.

7. Software Engineer in The Higher State College of Communication, in 2019 ended course of IOS-development in TeachMeSkills

8. Pre-Intermediate
