nielsen_selected_value = 
 VAR A = SELECTEDVALUE('Dim Period Nutripedia'[Current_Month_Desc])
   VAR B = SELECTEDVALUE('Dim Nielsen Geography Hierarchy'[nielsen_zone])
   VAR C = SELECTEDVALUE('Dim Nielsen Geography Hierarchy'[urb_rur])
   VAR D = SELECTEDVALUE('Dim Nielsen Geography Hierarchy'[nielsen_state])
   VAR E = SELECTEDVALUE('Dim Nielsen Product Hierarchy'[category])
   VAR F = SELECTEDVALUE('Dim Nielsen Product Hierarchy'[segment])
   VAR G = SELECTEDVALUE('Dim Nielsen Product Hierarchy'[stage])
   VAR H = SELECTEDVALUE('Dim Nielsen Product Hierarchy'[manufacturer])
   VAR I = SELECTEDVALUE('Dim Nielsen Product Hierarchy'[brand])
   VAR J = SELECTEDVALUE('Dim Nielsen Product Hierarchy'[subbrand])
   VAR TextA = IF(ISBLANK(A), " " , "Selected Month: " & A & UNICHAR(32) & "|")
   VAR TextB = IF(ISBLANK(B), " " , "Zone: " & B & UNICHAR(32) & "|")
   VAR TextC = IF(ISBLANK(C), " " , "URB/RUR: " & C & UNICHAR(32) & "|")
   VAR TextD = IF(ISBLANK(D), " " , "State: " & D & UNICHAR(32) & "|")
   VAR TextE = IF(ISBLANK(E), " " , "Category: " & E & UNICHAR(32) & "|")
   VAR TextF = IF(ISBLANK(F), " " , "Segment: " & F & UNICHAR(32) & "|")
   VAR TextG = IF(ISBLANK(G), " " , "Stage: " & G & UNICHAR(32) & "|")
   VAR TextH = IF(ISBLANK(H), " " , "Manufacturer: " & H & UNICHAR(32) & "|")
   VAR TextI = IF(ISBLANK(I), " " , "Brand: " & I & UNICHAR(32) & "|")
   VAR TextJ = IF(ISBLANK(J), " " , "Subbrand: " & J & UNICHAR(32) & "|")
   VAR SelectedText = 
       TextA & 
       TextB & 
       TextC & 
       TextD & 
       TextE & 
       TextF & 
       TextG &
       TextH &
       TextI & 
       TextJ 
   
   RETURN
       IF(ISBLANK(SelectedText), " " , SelectedText)
