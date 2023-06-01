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

       section Platon-UI-core-A/B
       Initialize Platon-UI-core-B         :active, fr1, 2023-05-25, 15d
       Tests for Platon-UI-core-B          :active, fr2, after fr1, 15d
       Documentation                       :active, fr3, after fr2, 2d

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
       Exclude auth module                           :           pc1, after pp3, 15d
       Exclude ui-module (File-manager)              :active,    fm1, after fr3, 5d
       Integration ui-module with Platon-UI-core-B   :active,    fm2, after fm1, 5d
       Writing tests for ui-module (File-manager)    :active,    fm3, after fm2, 10d
       Documentation for ui-module (File-manager)    :active,    fm4, after fm3, 2d

       section Platon modules (other module)
       Init backend                           :crit,    pa1, after pg3, 15d
       Exclude ui-modules.                    :active   ud1, after fm4, 21d
       Connect ui-modules with UI-core-B      :crit,    ui1, after ud1, 15d
       Exclude backend modules.               :active   em1, after ev1, 21d
       Initialize module.                     :active   om1, after em1, 15d

       section platon-admin (for configure/install/remove the platon-app and modules)
       Init backend                 :crit,    pa1, after pg3, 15d 
       Init UI                      :crit,    pu1, after ui1, 15d
       
       section Platon market-place
       Init backend                      :crit,    pa1, after pg3, 15d
       Init ui-core                      :crit,    uc1, after pu1, 21d
       
       section Documentation
       Init                      :crit,    pa1, after pg3, 15d 
       
       
   ```
