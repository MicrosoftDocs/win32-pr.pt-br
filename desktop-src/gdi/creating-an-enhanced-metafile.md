---
description: Esta seção contém um exemplo que demonstra a criação de um metarquivo avançado que é armazenado em um disco, usando um nome de arquivo especificado pelo usuário.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Criando um metarquivo avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e53266ac0677da211308c7028f4d61869fc2890f27c06daeff9cfb6fea87e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849226"
---
# <a name="creating-an-enhanced-metafile"></a>Criando um metarquivo avançado

Esta seção contém um exemplo que demonstra a criação de um metarquivo avançado que é armazenado em um disco, usando um nome de arquivo especificado pelo usuário.

O exemplo usa um contexto de dispositivo para a janela do aplicativo como o contexto do dispositivo de referência. (O sistema armazena os dados de resolução para esse dispositivo no cabeçalho do metarquivo avançado.) O aplicativo recupera um identificador que identifica esse contexto de dispositivo chamando a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .

O exemplo usa as dimensões da área do cliente do aplicativo para definir as dimensões do quadro de imagem. Usando as dimensões de retângulo retornadas pela função [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) , o aplicativo converte as unidades de dispositivo em unidades de 0,01-milímetro e passa os valores convertidos para a função [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .

O exemplo exibe uma caixa de diálogo **salvar como** comum que permite que o usuário especifique o nome do arquivo do novo metarquivo avançado. O sistema acrescenta a extensão. EMF de três caracteres a esse nome de arquivo e passa o nome para a função [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .

O exemplo também insere uma descrição de texto da imagem no cabeçalho Enhanced-Metafile. Essa descrição é especificada como um recurso na tabela de cadeia de caracteres do arquivo de recurso do aplicativo. No entanto, em um aplicativo funcional, essa cadeia de caracteres seria recuperada de um controle personalizado em uma caixa de diálogo comum ou de uma caixa de diálogo separada, exibida exclusivamente para essa finalidade.


```C++
// Obtain a handle to a reference device context.  
 
hdcRef = GetDC(hWnd); 
 
// Determine the picture frame dimensions.  
// iWidthMM is the display width in millimeters.  
// iHeightMM is the display height in millimeters.  
// iWidthPels is the display width in pixels.  
// iHeightPels is the display height in pixels  
 
iWidthMM = GetDeviceCaps(hdcRef, HORZSIZE); 
iHeightMM = GetDeviceCaps(hdcRef, VERTSIZE); 
iWidthPels = GetDeviceCaps(hdcRef, HORZRES); 
iHeightPels = GetDeviceCaps(hdcRef, VERTRES); 
 
// Retrieve the coordinates of the client  
// rectangle, in pixels.  
 
GetClientRect(hWnd, &rect); 
 
// Convert client coordinates to .01-mm units.  
// Use iWidthMM, iWidthPels, iHeightMM, and  
// iHeightPels to determine the number of  
// .01-millimeter units per pixel in the x-  
//  and y-directions.  
 
rect.left = (rect.left * iWidthMM * 100)/iWidthPels; 
rect.top = (rect.top * iHeightMM * 100)/iHeightPels; 
rect.right = (rect.right * iWidthMM * 100)/iWidthPels; 
rect.bottom = (rect.bottom * iHeightMM * 100)/iHeightPels; 
 
// Load the filename filter from the string table.  
 
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace the '%' separators that are embedded  
// between the strings in the string-table entry  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
 
// Load the dialog title string from the table.  
 
LoadString(hInst, IDS_TITLESTRING, 
     (LPSTR)szTitle, sizeof(szTitle)); 
 
// Initialize the OPENFILENAME members.  
 
szFile[0] = '\0'; 
 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrFile= szFile; 
Ofn.nMaxFile = sizeof(szFile)/ sizeof(*szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_OVERWRITEPROMPT; 
Ofn.lpstrTitle = szTitle; 
 
// Display the Filename common dialog box. The  
// filename specified by the user is passed  
// to the CreateEnhMetaFile function and used to  
// store the metafile on disk.  
 
GetSaveFileName(&Ofn); 
 
// Load the description from the string table.  
 
LoadString(hInst, IDS_DESCRIPTIONSTRING, 
     (LPSTR)szDescription, sizeof(szDescription)); 
 
// Replace the '%' string separators that are  
// embedded between strings in the string-table  
// entry with '\0'.  
 
for (i=0; szDescription[i]!='\0'; i++) 
{
    if (szDescription[i] == '%') 
            szDescription[i] = '\0'; 
}
 
// Create the metafile device context.  
 
hdcMeta = CreateEnhMetaFile(hdcRef, 
          (LPTSTR) Ofn.lpstrFile, 
          &rect, (LPSTR)szDescription); 
 
if (!hdcMeta) 
    errhandler("CreateEnhMetaFile", hWnd); 
 
// Release the reference device context.  
 
ReleaseDC(hWnd, hdcRef); 
```



 

 
