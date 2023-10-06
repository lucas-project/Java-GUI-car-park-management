image.png
image.png
This is a demo project which build a GUI using Java to do car management.
Homepage
![homepage](https://github.com/lucas-project/Java-GUI-car-park-management/assets/87470079/df074e94-1e71-4118-9643-b98b522af581)

Parking slot overview
![parking slot overview](https://github.com/lucas-project/Java-GUI-car-park-management/assets/87470079/39b73246-d2b6-4497-a057-8ef8f03d022c)

Components
# 1.JFrame frame   
Description: This a JFrame type component for making a frame that containing all other JComponents.
# 2. Container contentPane
Description: This an JFrame’s method to provide a container for all JComponents.
# 3. JPanel panel_btn  
Description: This panel is for placing all left-side buttons.
# 4. JPanel panel_welcome_info  
Description: This panel is on the top and for placing welcome words to users. 
# 5. JPanel panel_content_top 
Description: This panel is right under the panel_welcome_info and for displaying all parking slots.  
# 6. JPanel panel_content_bottom  
Description: This panel is placed on the bottom of the interface, it only be visible the first time user open the system, it contains input column for user to provide the quantity of staff slot and visitor slots to be created initially. 
# 7. JButton showAll   
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to display all parking slots when user click it.
# 8.JButton findCar  
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to search for a car when user click it. 
# 9. JButton parkCar   
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to park a car into a slot when user click it. User provide the car information and slot ID to park a car.
# 10. JButton deleteSlot  
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to delete a slot when user click it. User provide the slot ID to indicate which slot to be deleted.
# 11. JButton removeCar  
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to remove a car from a slot when user click it. 
# 12. JButton addParkingSlot  
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to add a new parking slot when user click it. 
# 13. JButton exitApplication   
Description: This button is on the left side and inside panel_btn, it attach to an event listener that enable user to exit the parking system when user click it.
# 14. JPanel createSlot  
Description: This panel is inside panel_content_bottom, it contains JComponent 16, 17, 18, 19, 20, 21 below, this part is for user to create staff and visitor slots the first time they using the parking system. 
# 15. JLabel welcomeLabel   
This label is on the top inside panel_content_top for displaying a welcome sentence to user.
# 16.JLabel Staff   
Description: This label is for displaying word “staff” to indicate the textfield’s purpose.
# 17. JLabel Visitor 
Description: This label is for displaying word “visitor” to indicate the textfield’s purpose.  
# 18. JLabel hints  
Description: This label is for displaying instruction to tell user to enter the quantity of staff and visitor slot to be created the first time for using the system. 
# 19. JButton confirmCreate  
Description: This button is a confirm button for created the amount of staff and visitor slot user entered. Once user pushed this button, the system will start creating slots and displaying the main interface of the system.
# 20. JTextField staffSlots  
Description: This text field is for user to provide the amount of staff slot to be created the first time using the system. 
# 21. JTextField visitorSlots  
Description: This text field is for user to provide the amount of visitor slot to be created the first time using the system. 
# 22.JButton Slots   
This is the component that represent the parking slots on the system, it’s created dynamically based on need, if user created 2 slots, then there will be two of this button display on the panel_content_top, but with different name by using setName() method.





2.GUI event handling functions
1.ActionListener  ShowAllListener()
Description: This action listener is triggered by clicking ‘showAll’ button, when it triggered, it will execute public ‘showAllSlot()’ method , which display all parking slots in panel_content_top.
2.ActionListener  FindCarListener()
Description: This action listener is triggered by clicking ‘findCar’ button, when it triggered, it will execute findACar() method , which enable user to enter a car registration number and search for the car.
3.ActionListener  ParkCarListener()
Description: This action listener is triggered by clicking ‘parkCar’ button, when it triggered, it will execute ‘parkACar()’ method , which allow user to enter their car registration number, owner name, user type and slot number to park a car into an existed slot.
4.ActionListener  DeleteSlotListener()
Description: This action listener is triggered by clicking ‘deleteSlot’ button, when it triggered, it will execute ‘deleteCarSlot()’ method , which allow user to provide a slot id to delete a slot with no car parking.
5.ActionListener  RemoveCarListener()
Description: This action listener is triggered by clicking ‘removeCar’ button, when it triggered, it will execute ‘removeACar()’ method , which allow user to remove a car from a slot by providing the car’s registration number.

6.ActionListener  AddParkingSlotListener1()
Description: This action listener is triggered by clicking ‘confirmCreate’ button, when it triggered, it will execute ‘addCarSlot1()’ method , which enable users to enter staff and visitor slot quantity to be created.

7.ActionListener  AddParkingSlotListener2()
Description: This action listener is triggered by clicking ‘addParkingSlot’ button, when it triggered, it will execute ‘addCarSlot2()’ method , which allow user to provide a slot ID to create a new parking slot.

8.ActionListener  ExitApplicationListener()
Description: This action listener is triggered by clicking ‘exitApplication’ button, when it triggered, it will execute ‘windowClose()’ method , which allow user to exit the system and close the current window.

9.ActionListener  ClickedSlotListener()
Description: This mouse listener is triggered by clicking ‘Slots’ button, when it triggered, it will provide 3 operation options for user to choose, they are ‘Park a car’, Remove a car’ and ‘Delete a slot’.
When user choose ‘Park a car’, the system will execute ‘clickParkcar(String slot_id)’ method, which allows user to park a car into a slot by clicking the slot, this method will catch the slot id of the slot clicked.
When user choose ‘Remove a car’, the system will execute ‘clickRemoveCar(String slot_id)’ method, which allow user to directly delete a car from a parking slot by clicking the slot, this method will detect the slot_id of the slot clicked.
When user choose ‘Delete a slot’, the system will execute ‘clickDeleteSlot(String slot_id)’ method, which allow user to directly delete a parking slot by clicking the slot, this method will detect the slot_id of the slot clicked.


10.MouseListener  ChangeColor()
Description: This mouse listener is for changing to buttons on the left side to different color when being clicked and entered.
