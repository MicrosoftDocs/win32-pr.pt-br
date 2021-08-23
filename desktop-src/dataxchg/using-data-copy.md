---
title: Usando a cópia de dados
description: Este tópico fornece um exemplo que demonstra como enviar informações entre dois aplicativos.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Windows Interface do usuário, cópia de dados
- cópia de dados, exemplos
- cópia de dados, WM_COPYDATA mensagem
- WM_COPYDATA mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231a03a30c578590dabf04d740f917a791a86d0e868d3587ff0b63bf283866f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730546"
---
# <a name="using-data-copy"></a>Usando a cópia de dados

O exemplo a seguir demonstra como enviar informações entre dois aplicativos usando a [**mensagem \_ CopyData do WM**](wm-copydata.md) .

O aplicativo de envio exibe uma caixa de diálogo para o usuário que solicita determinadas informações. O aplicativo empacota as informações em uma estrutura de dados privada, inclui um ponteiro para a estrutura na estrutura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) e envia as informações para o aplicativo de recebimento usando a [**mensagem \_ CopyData do WM**](wm-copydata.md) . O aplicativo de recebimento tem uma janela oculta com o nome de classe Disp32Class.


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



O aplicativo receptor tem uma janela oculta que recebe as informações do [**WM \_ CopyData**](wm-copydata.md) e a exibe para o usuário.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**FindWindow**](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 