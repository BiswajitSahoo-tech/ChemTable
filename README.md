# ChemTable
### A REPL CLI tool for quering periodic table
![2022-07-19](https://user-images.githubusercontent.com/73599660/179800225-3858402d-bac8-4cce-afd4-5ca4fb489e30.png)
![2022-07-19 (3)](https://user-images.githubusercontent.com/73599660/179800345-bd80acc3-3358-44d9-950e-5c1be2d86bc0.png)
![2022-07-19 (1)](https://user-images.githubusercontent.com/73599660/179800382-00927a31-5e0f-406c-8e8b-25ca7dac4b39.png)

#### Available Commands
 **Possible combinations of Commands in this version are**
        Command                                         Description

        get <p> <q> <r>                        Give all the property value of an element specified with row,column,f-block element or not. e,g : get 1 1 0.
                                               p = period number, q = group number, r = 0 if element is not f-block else no. of element from starting of block.

        get <p> <q> <r> <property name>        Same as above but shows only specific property value as given their. e,g: get 1 1 0 mp.
        get <p> <q> <r> state <K> <degree>     Same as above but shows only state value as given their. e,g: get 1 1 0 state at 100.
                                               Temperature in celcius scale & K is State command
        get <series name >                     Shows all the property of all the elements of given series. e,g: get 3d.
        get <series name> <property name>      Shows given property value of all the element of given series. e,g: get 3d density.
        get block <block name >                Shows all the property of all the elements of given block. e,g: get D.
        get block <block name> <property name> Shows given property value of all the element of given block. e,g: get P density.
        get <Group name >                      Shows all the property of all the elements of given . e,g: get alkaline.
        get <Group name> <property name>       Shows given property value of all the element of given block. e,g: get alkali density.
        set <p> <q> <r> <property> <newValue>  Setting of new value of given property of given elements

        plot <series> <property>               Making Graph of given series of given property

        sort <series> <property>               Sorting element of given series with respect to given property value


              Property Command           Description

                       density           For Desity
                            mp           For Melting Point
                            bp           For Boiling Point
                            en           For Electro Nagetivity
                            ip           For Ionisation Potential
                          atmN           For Atomic Number
                          atmR           For Atomic Radius
                          name           For Name
                           sym           For Symbol
                          atmW           For Atomic Weight
                         state           For Physical State
                           all           For All Properties


                Group Commands           Description

                        alkali           For Alkali Group
                 alkali_metals           For Alkali Group
                alkaline_earth           For Alkaline Group
         alkaline_earth_metals           For Alkaline Group
                  boron_family           For Boron Family
                 carbon_family           For Carbon Family
                      pricogen           For Pricogen Family
                     pricogens           For Pricogen Family
                    chalcogens           For Chalcogen Family
                     chalcogen           For Chalcogen Family
                       halogen           For Halogen Family
                      halogens           For Halogen Family
                     nobel_gas           For Nobel Gas
                   nobel_gases           For Nobel Gas


                State Commands           Description

                            at           For Perticular Temperature
                         after           For Above Temerature
                        before           For Below Temperature


#### File Details
* **cli:** This file contains the introductory design and its code. Help command code is also in this file.
* **element:** This file contains the codes for all the data structures.
* **cmd.fun:** As the name itself depicts that this file contains codes for all the command functions.
* **Book1:** This excel file has list of datas. This is not importanr for the application.
* **pencil:** This is the main c file for the application. 
* **Pencil Application:** This is the exe file which you can run it on your machine.

#### Approach
We store data about all the element in binaryList.bin, choosing binary file format save space. On running the application, it create a linked list structure simillar to periodic table on the memory by reading data present on binaryList.bin file. We later use this data structure for giving answer to all of our query.

#### Additional Information
* Any change or modification in the code must be done by [Creating another branch](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository#:~:text=Further%20reading-,Creating%20a%20branch,main%20page%20of%20the%20repository.&text=Click%20the%20branch%20selector%20menu,branch%2C%20then%20select%20Create%20branch.).
* **Branch creating format:** yourname#serial-number For example: *biswajit#01*
* Branch is compulsory so that the main source code remains protected.
* Later code will be reviewed and merged with the main branch.
* In the file Book1, 0 indicates that the element is not present in the f-block and non-zero numbers indicates that the element is present in the f-block and their serial.
