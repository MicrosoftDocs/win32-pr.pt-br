---
title: Usando a cópia de dados
description: Este tópico fornece um exemplo que demonstra como enviar informações entre dois aplicativos.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Interface do usuário do Windows, cópia de dados
- cópia de dados, exemplos
- cópia de dados, WM_COPYDATA mensagem
- WM_COPYDATA mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e44c4abb9aba68d4db1544f5c7d52220cdc681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782431"
---
# <a name="using-data-copy"></a><span data-ttu-id="ade92-107">Usando a cópia de dados</span><span class="sxs-lookup"><span data-stu-id="ade92-107">Using Data Copy</span></span>

<span data-ttu-id="ade92-108">O exemplo a seguir demonstra como enviar informações entre dois aplicativos usando a [**mensagem \_ CopyData do WM**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="ade92-108">The following example demonstrates how to send information between two applications using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span>

<span data-ttu-id="ade92-109">O aplicativo de envio exibe uma caixa de diálogo para o usuário que solicita determinadas informações.</span><span class="sxs-lookup"><span data-stu-id="ade92-109">The sending application displays a dialog box to the user which requests certain information.</span></span> <span data-ttu-id="ade92-110">O aplicativo empacota as informações em uma estrutura de dados privada, inclui um ponteiro para a estrutura na estrutura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) e envia as informações para o aplicativo de recebimento usando a [**mensagem \_ CopyData do WM**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="ade92-110">The application packages the information into a private data structure, includes a pointer to the structure in the [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure, and sends the information to the receiving application using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span> <span data-ttu-id="ade92-111">O aplicativo de recebimento tem uma janela oculta com o nome de classe Disp32Class.</span><span class="sxs-lookup"><span data-stu-id="ade92-111">The receiving application has a hidden window with the class name Disp32Class.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



<span data-ttu-id="ade92-112">O aplicativo receptor tem uma janela oculta que recebe as informações do [**WM \_ CopyData**](wm-copydata.md) e a exibe para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ade92-112">The receiving application has a hidden window which receives the information from [**WM\_COPYDATA**](wm-copydata.md) and displays it to the user.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a><span data-ttu-id="ade92-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ade92-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ade92-114">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ade92-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ade92-115">**FindWindow**</span><span class="sxs-lookup"><span data-stu-id="ade92-115">**FindWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 