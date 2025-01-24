
---
title: Example Structure of a Military Joint Force Group Executing a Fix Drill
---
erDiagram
    HQ ELEMENT ||--|{ ALPHA COMM TEAM : coordinates/sends orders
    HQ ELEMENT ||--|{ BRAVO COMM TEAM : coordinates/sends orders
    HQ ELEMENT {
        command team
    } 
    ALPHA 6 COMM TEAM ||--|{ HQ ELEMENT : sends SITREP/receives orders
    ALPHA 6 COMM TEAM ||--|{ ALPHA 1 FIX ELEMENT : coordinates
    ALPHA 6 COMM TEAM ||--|{ ALPHA 2 MANEUVER ELEMENT : coordinates
    ALPHA 6 COMM TEAM ||--|{ REMOTE FIRE SUPPORT : requests fire support
    ALPHA 6 COMM TEAM {
        command team
    }    
    BRAVO 6 COMM TEAM ||--|{ HQ ELEMENT : sends SITREP/receives orders
    BRAVO 6 COMM TEAM ||--|{ BRAVO 1 OVERWATCH ELEMENT
    BRAVO 6 COMM TEAM ||--|{ BRAVO 2 SECURITY ELEMENT
    BRAVO 6 COMM TEAM ||--|{ BRAVO 3 JTAC ELEMENT
    BRAVO 6 COMM TEAM {
        command team
    }   
    BRAVO 1 OVERWATCH ELEMENT ||--|{ BRAVO 6 COMM TEAM : sends SITREP
    BRAVO 1 OVERWATCH ELEMENT ||--|{ ALPHA 1 FIX ELEMENT : provides visual feedback
    BRAVO 1 OVERWATCH ELEMENT ||--|{ ALPHA 2 MANEUVER ELEMENT : provides visual feedback 
    BRAVO 1 OVERWATCH ELEMENT {
        sniper team
        weapons team
    }
    BRAVO 2 SECURITY ELEMENT ||--{ BRAVO 6 COMM TEAM : sends SITREP
    BRAVO 2 SECURITY ELEMENT ||--{ BRAVO 1 OVERWATCH ELEMENT : coordinates with 
    BRAVO 2 SECURITY ELEMENT }|..|{ ALPHA 1 FIX ELEMENT : supports/covers
    BRAVO 2 SECURITY ELEMENT }|..|{ ALPHA 2 MANEUVER ELEMENT : supports/covers
    BRAVO 2 SECURITY ELEMENT ||--o{ OPFOR ELEMENT 2 : engages on approach
    BRAVO 2 SECURITY ELEMENT {
        security team1 
        security team2 
        security team3  
    }
    BRAVO 3 JTAC ELEMENT ||--|{ BRAVO 6 COMM TEAM : sends SITREP
    BRAVO 3 JTAC ELEMENT ||--|{ COBRA 1 CLOSE AIR SUPPORT : 
    BRAVO 3 JTAC ELEMENT ||--|{ DAGGER 1 CLOSE AIR SUPPORT : 
    BRAVO 3 JTAC ELEMENT ||--|{ ALPHA 6 COMM TEAM : coordinates with 
    BRAVO 3 JTAC ELEMENT ||--o{ OPFOR ELEMENT 2 : engages via C.A.S.
    BRAVO 3 JTAC ELEMENT {
        JTAC team
        DART team
    }    
    ALPHA 1 FIX ELEMENT ||--|{ ALPHA 6 COMM TEAM : sends SITREP
    ALPHA 1 FIX ELEMENT ||--|{ ALPHA 2 MANEUVER ELEMENT : coordinates with  
    ALPHA 1 FIX ELEMENT ||--o{ OPFOR ELEMENT 1 : supresses/fixes
    ALPHA 1 FIX ELEMENT {
        HMG team1
        HMG team2
        Rifle team
        AT team
    }
    ALPHA 2 MANEUVER ELEMENT ||--|{ ALPHA 6 COMM TEAM : sends SITREP
    ALPHA 2 MANEUVER ELEMENT ||--|{ ALPHA 1 FIX ELEMENT : coordinates with
    ALPHA 2 MANEUVER ELEMENT ||--o{ OPFOR ELEMENT 1 : flanks/closes with/destroys
    ALPHA 2 MANEUVER ELEMENT {
        Infantry squad x 4
    }    
    COBRA 1 CLOSE AIR SUPPORT ||--o{ BRAVO 3 JTAC ELEMENT : engages designated targets
    COBRA 1 CLOSE AIR SUPPORT {
        C-130X 
    }
    DAGGER 1 CLOSE AIR SUPPORT ||--o{ BRAVO 3 JTAC ELEMENT : engages designated targets
    DAGGER 1 CLOSE AIR SUPPORT {
        AH-64D x2 
    }    
    REMOTE FIRE SUPPORT }|..|{ ALPHA 6 COMM TEAM : supports
    REMOTE FIRE SUPPORT }|..|{ BRAVO 6 COMM TEAM : supports
    REMOTE FIRE SUPPORT }|..|{ BRAVO 1 OVERWATCH ELEMENT : supports
    REMOTE FIRE SUPPORT {
        battery company
    }
    OPFOR ELEMENT 1 ||--|{ OPFOR ELEMENT 2 : maintains communication
    OPFOR ELEMENT 1 {
        infantry regulars
    }
    OPFOR ELEMENT 2 }|..|{ OPFOR ELEMENT 1 : supports 
    OPFOR ELEMENT 2 {
        infantry mechanized
    }    
















    
    
