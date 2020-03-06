# Eugene Stefanovich

## Contact info
    - e-mail: mejogi000@gmail.com
    - mobile/telegram: +375296690010
    - linkedin: [Eugene Stefanovich](https://www.linkedin.com/in/eugene-stefanovich-b5a2a7170/)

## Skills
- programming language - swift
- good knowledge main tools swift development such as Xcode, Storyboard, GitHub, BitBucket and others
- good knowledge main frameworks iOS SDK (Foundation, UIKit and others)
- knowledge CoreData, Realm, Alamofire and other
- knowledge main design patterns and principles of object oriented programming
- understanding the principles of work client-server and mobile applications 

## Code exapmles (ARKit framework)
```Swift
import SceneKit
import ARKit

class Plane: SCNNode {
    
    var anchor: ARPlaneAnchor!
    var planeGeometry: SCNPlane!
    
    init(anchor: ARPlaneAnchor) {
        self.anchor = anchor
        super.init()
        configure()
    }
    
    private func configure() {
        
        self.planeGeometry = SCNPlane(width: CGFloat(anchor.extent.x), height: CGFloat(anchor.extent.z))
        
        let material = SCNMaterial()
        material.diffuse.contents = UIColor.clear // UIImage(named: "pinkWeb.png")
        
        self.planeGeometry.materials = [material]
        
        self.geometry = planeGeometry
        
        let physicsShape = SCNPhysicsShape(geometry: self.geometry!, options: nil)
        self.physicsBody = SCNPhysicsBody(type: .static, shape: physicsShape)
        self.physicsBody?.categoryBitMask = BitMaskCategory.plane
        self.physicsBody?.collisionBitMask = BitMaskCategory.box
        self.physicsBody?.contactTestBitMask = BitMaskCategory.box
        
        self.position = SCNVector3(anchor.center.x, 0, anchor.center.z)
        
        self.transform = SCNMatrix4MakeRotation(Float(-Double.pi / 2), 1.0, 0.0, 0.0)
    }
    
    func update(anchor: ARPlaneAnchor) {
        
        self.planeGeometry.width = CGFloat(anchor.extent.x)
        self.planeGeometry.height = CGFloat(anchor.extent.z)
        self.position = SCNVector3(anchor.center.x, 0, anchor.center.z)
    }
    
    required init?(coder aDecoder: NSCoder) {
        fatalError("init(coder:) has not been implemented")
    }
}
```
## Education

#### 2003-2009
Software Engineer in The Higher State College of Communication

#### 2019
Course of IOS-development in TeachMeSkills
