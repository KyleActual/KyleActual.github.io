```mermaid
---
title: Example Structure of a Military Joint Force Group Executing a Fix Drill
---
erDiagram
    HQ_ELEMENT ||--|{ ALPHA_6_COMM_TEAM : coordinates-and-directs
    HQ_ELEMENT ||--|{ BRAVO_6_COMM_TEAM : coordinates-and-directs
    HQ_ELEMENT {
        command team
    } 
    ALPHA_6_COMM_TEAM ||--|{ HQ_ELEMENT : sends-SITREP-and-relays-orders
    ALPHA_6_COMM_TEAM ||--|{ ALPHA_1_FIX_ELEMENT : coordinates
    ALPHA_6_COMM_TEAM ||--|{ ALPHA_2_MANEUVER_ELEMENT : coordinates
    ALPHA_6_COMM_TEAM ||--|{ REMOTE_FIRE_SUPPORT : requests-fire-support
    ALPHA_6_COMM_TEAM {
        command team
    }    
    BRAVO_6_COMM_TEAM ||--|{ HQ_ELEMENT : sends-SITREP-and-relays-orders
    BRAVO_6_COMM_TEAM ||--|{ BRAVO_1_OVERWATCH_ELEMENT : coordinates-and-directs
    BRAVO_6_COMM_TEAM ||--|{ BRAVO_2_SECURITY_ELEMENT : coordinates-and-directs
    BRAVO_6_COMM_TEAM ||--|{ BRAVO_3_JTAC_ELEMENT : coordinates-and-directs
    BRAVO_6_COMM_TEAM {
        command team
    }   
    BRAVO_1_OVERWATCH_ELEMENT ||--|{ BRAVO_6_COMM_TEAM : sends-SITREP-and-executes-orders
    BRAVO_1_OVERWATCH_ELEMENT ||--|{ ALPHA_1_FIX_ELEMENT : visual-feedback
    BRAVO_1_OVERWATCH_ELEMENT ||--|{ ALPHA_2_MANEUVER_ELEMENT : visual-feedback
    BRAVO_1_OVERWATCH_ELEMENT ||--o{ OPFOR_ELEMENT_1 : observes
    BRAVO_1_OVERWATCH_ELEMENT ||--o{ OPFOR_ELEMENT_2 : observes
    BRAVO_1_OVERWATCH_ELEMENT {
        sniper team
        weapons team
    }
    BRAVO_2_SECURITY_ELEMENT ||--|{ BRAVO_6_COMM_TEAM : sends-SITREP-and-executes-orders
    BRAVO_2_SECURITY_ELEMENT ||--|{ BRAVO_1_OVERWATCH_ELEMENT : coordinates
    BRAVO_2_SECURITY_ELEMENT }|..|{ ALPHA_1_FIX_ELEMENT : supports-and-covers
    BRAVO_2_SECURITY_ELEMENT }|..|{ ALPHA_2_MANEUVER_ELEMENT : supports-and-covers
    BRAVO_2_SECURITY_ELEMENT ||--o{ OPFOR_ELEMENT_1 : engages-flanking-elements
    BRAVO_2_SECURITY_ELEMENT ||--o{ OPFOR_ELEMENT_2 : engages-approaching-enemy-reinforcements 
    BRAVO_2_SECURITY_ELEMENT {
        security team1 
        security team2 
        security team3  
    }
    BRAVO_3_JTAC_ELEMENT ||--|{ BRAVO_6_COMM_TEAM : sends-SITREP-and-executes-orders
    BRAVO_3_JTAC_ELEMENT ||--|{ COBRA_1_CLOSE_AIR_SUPPORT : designates-targets
    BRAVO_3_JTAC_ELEMENT ||--|{ DAGGER_1_CLOSE_AIR_SUPPORT : designates-targets
    BRAVO_3_JTAC_ELEMENT ||--o{ OPFOR_ELEMENT_1 : relays-position-to-CAS
    BRAVO_3_JTAC_ELEMENT ||--o{ OPFOR_ELEMENT_2 : relays-position-to-CAS
    BRAVO_3_JTAC_ELEMENT {
        JTAC team
        DART team
    }    
    ALPHA_1_FIX_ELEMENT ||--|{ ALPHA_6_COMM_TEAM : sends-SITREP-and-executes-orders
    ALPHA_1_FIX_ELEMENT ||--|{ ALPHA_2_MANEUVER_ELEMENT : coordinates  
    ALPHA_1_FIX_ELEMENT ||--o{ OPFOR_ELEMENT_1 : supresses-and-fixes
    ALPHA_1_FIX_ELEMENT {
        HMG team1
        HMG team2
        Rifle team
        AT team
    }
    ALPHA_2_MANEUVER_ELEMENT ||--|{ ALPHA_6_COMM_TEAM : sends-SITREP-and-executes-orders
    ALPHA_2_MANEUVER_ELEMENT ||--|{ ALPHA_1_FIX_ELEMENT : coordinates 
    ALPHA_2_MANEUVER_ELEMENT ||--o{ OPFOR_ELEMENT_1 : closes-with-and-destroys
    ALPHA_2_MANEUVER_ELEMENT {
        engagement-team x4
    }    
    COBRA_1_CLOSE_AIR_SUPPORT ||--|{ BRAVO_3_JTAC_ELEMENT : recieves-target-data
    COBRA_1_CLOSE_AIR_SUPPORT ||--o{ OPFOR_ELEMENT_1 : observes
    COBRA_1_CLOSE_AIR_SUPPORT ||--o{ OPFOR_ELEMENT_2 : engages
    COBRA_1_CLOSE_AIR_SUPPORT {
        C-130X x1
    }
    DAGGER_1_CLOSE_AIR_SUPPORT ||--|{ BRAVO_3_JTAC_ELEMENT : recieves-target-data
    DAGGER_1_CLOSE_AIR_SUPPORT ||--o{ OPFOR_ELEMENT_2 : engages
    DAGGER_1_CLOSE_AIR_SUPPORT {
        AH-64D x2 
    }    
    REMOTE_FIRE_SUPPORT }|..|{ ALPHA_6_COMM_TEAM : supports
    REMOTE_FIRE_SUPPORT }|..|{ BRAVO_6_COMM_TEAM : supports
    REMOTE_FIRE_SUPPORT }|..|{ BRAVO_1_OVERWATCH_ELEMENT : supports
    REMOTE_FIRE_SUPPORT {
        battery company
    }
    OPFOR_ELEMENT_1 ||--|{ OPFOR_ELEMENT_2 : maintains-communication
    OPFOR_ELEMENT_1 {
        infantry regulars
    }
    OPFOR_ELEMENT_2 }|..|{ OPFOR_ELEMENT_1 : supports 
    OPFOR_ELEMENT_2 {
        infantry mechanized
    }    
```
***
# EXPLANATION

The above diagram displays an example of the elements involved in one segment of a military joint task force operation simulated in Arma 3. Arma 3 is a military simulator used by the U.S. Army for a variety of virtual training modules. It is capable of simulating all aspects of a real world scenario, using real military units, equipment, tactics, and real-world open terrain.

In the scenario, the task force is executing a fix drill. In the fix drill, there are two main elements - the fixing element and the maneuvering element. The fixing element engages the target with sustained suppressive fire rendering them temporarily immobilized or 'fixed' in one position. While the target is fixed and unable to move freely, the maneuvering element advances - most often from a flank position - and engages the target directly from a much closer distance. The maneuver element then continues to close distance with and eventually overrun the target position. Despite the simplicity of this single task, the main elements nonetheless rely on a substantial network of supporting elements spanning multiple branches of the armed forces.    

## ENTITIES
- HQ ELEMENT - Headquarters element which contains the command team
- OVERWATCH - observes battlefield from a distant vantage point
- SECURITY - Guards exposed flanks and rear of other elements
- JTAC - Joint Tactical Air Controller - communicates directly with close air support units while embedded with units on the ground
- DART - Deployed Aircraft Response Team - responds to emergencies involving currently deployed air assets
- CLOSE AIR SUPPORT - aircraft currently in the vicinity providing support to ground units
- REMOTE FIRE SUPPORT - long range artillery from available battery units
- OPFOR - opposition forces

## RELATIONSHIP SPECIFICATIONS 
- coordinates-and-directs - maintains a birds-eye-view of the battlespace, tracks the location of all entitites and directs individual units.
- sends-SITREP-and-relays-orders - updates the command element with SITREPs (situation report), and relays orders from the HQ element to its subordinate elements
- coordinates - maintains communication with in order to synchronize movements and prevent friendly fire
- observes - maintains visual contact with and tracks the movements of target elements 
- supports-and-covers - secures exposed flanks and rear positions of the attacking elements 
- visual-feedback - real-time updates on battlefield movements 
- designates-targets - assigns targets to supporting units
- relays-position-to-CAS - determines the global position of a target and relays the location coordinates to close air support units 
- supresses-and-fixes - initiates sustained suppressive fire in order to immobilize a target and allow friendly forces to move freely
- recieves-target-data - recives the location of a target via the aircrafts head up display, relayed by a laser designator on the ground, and engages the target with laser guided weaponry.  
- sends-SITREP-and-executes-orders - updates its command element with SITREPs and directly executes orders. 

***





















    
    
