---
description: Esta seção explica como executar as seguintes tarefas associadas às propriedades da janela.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Usando propriedades de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771373"
---
# <a name="using-window-properties"></a><span data-ttu-id="9b31b-103">Usando propriedades de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-103">Using Window Properties</span></span>

<span data-ttu-id="9b31b-104">Esta seção explica como executar as seguintes tarefas associadas às propriedades da janela.</span><span class="sxs-lookup"><span data-stu-id="9b31b-104">This section explains how to perform the following tasks associated with window properties.</span></span>

-   [<span data-ttu-id="9b31b-105">Adicionando uma propriedade de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-105">Adding a Window Property</span></span>](#adding-a-window-property)
-   [<span data-ttu-id="9b31b-106">Recuperando uma propriedade de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-106">Retrieving a Window Property</span></span>](#retrieving-a-window-property)
-   [<span data-ttu-id="9b31b-107">Listando propriedades da janela para uma determinada janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-107">Listing Window Properties for a Given Window</span></span>](#listing-window-properties-for-a-given-window)
-   [<span data-ttu-id="9b31b-108">Excluindo uma propriedade de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-108">Deleting a Window Property</span></span>](#deleting-a-window-property)

## <a name="adding-a-window-property"></a><span data-ttu-id="9b31b-109">Adicionando uma propriedade de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-109">Adding a Window Property</span></span>

<span data-ttu-id="9b31b-110">O exemplo a seguir carrega um ícone e, em seguida, um cursor e aloca memória para um buffer.</span><span class="sxs-lookup"><span data-stu-id="9b31b-110">The following example loads an icon and then a cursor and allocates memory for a buffer.</span></span> <span data-ttu-id="9b31b-111">Em seguida, o exemplo usa a função [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) para atribuir o ícone resultante, o cursor e os identificadores de memória como propriedades de janela para a janela identificada pela variável hwndSubclass definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b31b-111">The example then uses the [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) function to assign the resulting icon, cursor, and memory handles as window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="9b31b-112">As propriedades são identificadas pelo ícone de PROP de cadeias de caracteres \_ , \_ cursor de prop e \_ buffer prop.</span><span class="sxs-lookup"><span data-stu-id="9b31b-112">The properties are identified by the strings PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span>


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



## <a name="retrieving-a-window-property"></a><span data-ttu-id="9b31b-113">Recuperando uma propriedade de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-113">Retrieving a Window Property</span></span>

<span data-ttu-id="9b31b-114">Uma janela pode criar identificadores para seus dados de propriedade de janela e usar os dados para qualquer finalidade.</span><span class="sxs-lookup"><span data-stu-id="9b31b-114">A window can create handles to its window property data and use the data for any purpose.</span></span> <span data-ttu-id="9b31b-115">O exemplo a seguir usa [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) para obter identificadores para as propriedades de janela identificadas pelo \_ ícone PROP, \_ cursor prop e \_ buffer prop.</span><span class="sxs-lookup"><span data-stu-id="9b31b-115">The following example uses [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) to obtain handles to the window properties identified by PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span> <span data-ttu-id="9b31b-116">Em seguida, o exemplo exibe o conteúdo do buffer de memória, do cursor e do ícone recentemente obtidos na área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="9b31b-116">The example then displays the contents of the newly obtained memory buffer, cursor, and icon in the window's client area.</span></span>


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



## <a name="listing-window-properties-for-a-given-window"></a><span data-ttu-id="9b31b-117">Listando propriedades da janela para uma determinada janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-117">Listing Window Properties for a Given Window</span></span>

<span data-ttu-id="9b31b-118">No exemplo a seguir, a função [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) lista os identificadores de cadeia de caracteres das propriedades da janela para a janela identificada pela variável hwndSubclass definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b31b-118">In the following example, the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function lists the string identifiers of the window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="9b31b-119">Essa função depende da função de retorno de chamada definida pelo aplicativo WinPropProc para exibir as cadeias de caracteres na área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="9b31b-119">This function relies on the application-defined callback function WinPropProc to display the strings in the window's client area.</span></span>


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



## <a name="deleting-a-window-property"></a><span data-ttu-id="9b31b-120">Excluindo uma propriedade de janela</span><span class="sxs-lookup"><span data-stu-id="9b31b-120">Deleting a Window Property</span></span>

<span data-ttu-id="9b31b-121">Quando uma janela é destruída, ela deve destruir todas as propriedades de janela definidas.</span><span class="sxs-lookup"><span data-stu-id="9b31b-121">When a window is destroyed, it must destroy any window properties it set.</span></span> <span data-ttu-id="9b31b-122">O exemplo a seguir usa a função [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) e a função de retorno de chamada definida pelo aplicativo DelPropProc para destruir as propriedades associadas à janela identificada pela variável hwndSubclass definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b31b-122">The following example uses the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function and the application-defined callback function DelPropProc to destroy the properties associated with the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="9b31b-123">A função de retorno de chamada, que usa a função [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) , também é mostrada.</span><span class="sxs-lookup"><span data-stu-id="9b31b-123">The callback function, which uses the [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) function, is also shown.</span></span>


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



 

 
