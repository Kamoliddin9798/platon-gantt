# Welcome to Platon core development team!

# Roadmap

```mermaid
gantt
       dateFormat  YYYY-MM-DD
       title Platon core roadmap

       section platon-discovery
       Initialize discovery                :done,    pd1, 2023-03-17, 15d
       Integration with Nats               :done,    pd2, after pd1, 15d
       Integration with Gateway            :done,    pd3, after pg1, 15d
       Fix bug 503 with platon-gateway     :active,  crit, after pd3, 20d
       
       section platon-gateway
       Initialize gateway                 :done,    pg1, 2023-03-17, 15d
       Integration with Nats              :done,    pg2, after pg1, 15d
       Integration with Discovery         :done,    pg3, after pd1, 15d
       
       section platon-auth
       Initialize auth                    :done,    pa1, after pg3, 15d
       Integration with Nats              :done,    pa2, after pa1, 15d
       Integration with Discovery         :done,    pa3, after pa1, 15d
       Auth UI                            :         after pa3, 20d
       
       section platon-plugin (Library for Spring boot application)
       Initialize plugin         :active,   pp1, 2023-05-19, 15d
       Download public key       :done,     pp2, after pp1, 3d
       Bulid into module         :          pp3, after pp1, 15d
       
       section platon-core (main module)
       Exclude auth module       :           pc1, after pp3, 15d
       Init                      :crit,      pa1, after pg3, 15d

       section Platon modules (other module)
       Init                      :crit,    pa1, after pg3, 15d 
       
       section platon-admin (for configure/install/remove the platon-app and modeules)
       Init                      :crit,    pa1, after pg3, 15d 
       
       section Platon market-place
       Init                      :crit,    pa1, after pg3, 15d 
       
       section Documentation
       Init                      :crit,    pa1, after pg3, 15d 

       section Critical tasks
       Init                      :crit,    pa1, after pg3, 15d 

       section Last section
       Init                      :crit,    pa1, after pg3, 15d 

       section Platon-frontend-starter
       Initialize frontend-starter         :active, fr1, 2023-05-25, 15d
       Writing tests for starter           :active, fr2, after fr1, 15d
       Documentation                       :active, fr3, after fr2, 2d

       section First module (File-manager)
       Initialize module                   :done,   fm1, 2023-04-15, 5d
       Integration module with starter     :active, fm2, after fr3, 5d
       Writing tests for module            :active, fm3, after fm2, 10d
       Documentation                       :active, fm4, after fm3, 2d
      
   ```
