---
description: Esta seção explica como executar as seguintes tarefas associadas às propriedades da janela.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Usando propriedades de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fcb4cb0346554ee2df5c1b2fc92df7675cd61d11799b891156b13f26fb213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028264"
---
# <a name="using-window-properties"></a>Usando propriedades de janela

Esta seção explica como executar as seguintes tarefas associadas às propriedades da janela.

-   [Adicionando uma propriedade de janela](#adding-a-window-property)
-   [Recuperando uma propriedade de janela](#retrieving-a-window-property)
-   [Listando propriedades da janela para uma determinada janela](#listing-window-properties-for-a-given-window)
-   [Excluindo uma propriedade de janela](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>Adicionando uma propriedade de janela

O exemplo a seguir carrega um ícone e, em seguida, um cursor e aloca memória para um buffer. Em seguida, o exemplo usa a função [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) para atribuir o ícone resultante, o cursor e os identificadores de memória como propriedades de janela para a janela identificada pela variável hwndSubclass definida pelo aplicativo. As propriedades são identificadas pelo ícone de PROP de cadeias de caracteres \_ , \_ cursor de prop e \_ buffer prop.


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a>Recuperando uma propriedade de janela

Uma janela pode criar identificadores para seus dados de propriedade de janela e usar os dados para qualquer finalidade. O exemplo a seguir usa [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) para obter identificadores para as propriedades de janela identificadas pelo \_ ícone PROP, \_ cursor prop e \_ buffer prop. Em seguida, o exemplo exibe o conteúdo do buffer de memória, do cursor e do ícone recentemente obtidos na área do cliente da janela.


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a>Listando propriedades da janela para uma determinada janela

No exemplo a seguir, a função [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) lista os identificadores de cadeia de caracteres das propriedades da janela para a janela identificada pela variável hwndSubclass definida pelo aplicativo. Essa função depende da função de retorno de chamada definida pelo aplicativo WinPropProc para exibir as cadeias de caracteres na área do cliente da janela.


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a>Excluindo uma propriedade de janela

Quando uma janela é destruída, ela deve destruir todas as propriedades de janela definidas. O exemplo a seguir usa a função [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) e a função de retorno de chamada definida pelo aplicativo DelPropProc para destruir as propriedades associadas à janela identificada pela variável hwndSubclass definida pelo aplicativo. A função de retorno de chamada, que usa a função [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) , também é mostrada.


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
