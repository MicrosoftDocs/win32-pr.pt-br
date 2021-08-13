---
title: Detectando e acompanhando vários pontos de toque
description: Detectando e acompanhando vários pontos de toque
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Toque, vários pontos de toque
- detectando vários pontos de toque
- acompanhamento de vários pontos de toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5b8086988dc1a87b5596d5a0ac74ec1f1df5ce4b85d928cbe306b791d17b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436036"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Detectando e acompanhando vários pontos de toque

As etapas a seguir explicam como rastrear vários pontos de toque usando Windows Touch.

1.  Crie um aplicativo e habilita Windows Touch.
2.  Adicione um manipulador para [**WM \_ TOUCH e**](wm-touchdown.md) pontos de controle.
3.  Desenhar os pontos.

Depois que o aplicativo é executado, ele renderiza círculos em cada toque. A captura de tela a seguir mostra a aparência do aplicativo durante a execução.

![captura de tela mostrando um aplicativo que renderiza pontos de toque como círculos verdes e amarelos](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Criar um aplicativo e habilitar o Windows Touch

Comece com um aplicativo Microsoft Win32 usando o assistente Microsoft Visual Studio aplicativo. Depois de concluir o assistente, adicione suporte para mensagens Windows Touch definindo Windows versão do Windows em targetver.h e incluindo windows.h e windowsx.h em seu aplicativo. O código a seguir mostra como definir a versão Windows em targetver.h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



O código a seguir mostra como suas diretivas de inclusão devem ser adicionadas. Além disso, você pode criar algumas variáveis globais que serão usadas posteriormente.


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a>Adicionar manipulador para WM \_ TOUCH e pontos de controle

Primeiro, declare algumas variáveis que são usadas pelo manipulador [**WM \_ TOUCH**](wm-touchdown.md) no [**WndProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Agora, inicialize as variáveis usadas para armazenar pontos de toque e registre a janela para entrada de toque do **método InitInstance.**


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



Em seguida, manipular [**a mensagem WM \_ TOUCH**](wm-touchdown.md) do [**método WndProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) O código a seguir mostra uma implementação do manipulador para **WM \_ TOUCH.**


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> Para usar a função [**ScreenToClient,**](/windows/desktop/api/winuser/nf-winuser-screentoclient) você deve ter suporte de DPI alto em seu aplicativo. Para obter mais informações sobre como dar suporte a alto DPI, consulte a [seção DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) alto do MSDN.

 

Agora, quando um usuário toca na tela, as posições que ele está tocando serão armazenadas na matriz de pontos. O **membro dwID** da estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) armazena um identificador que será dependente de hardware.

Para resolver o problema do membro dwID dependente de hardware, o manipulador de caso [**WM \_ TOUCH**](wm-touchdown.md) usa uma função, **GetContactIndex**, que mapeia o membro **dwID** da estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) para um ponto desenhado na tela. O código a seguir mostra uma implementação dessa função.


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a>Desenhar os pontos

Declare as seguintes variáveis para a rotina de desenho.


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



O *memDC* do contexto de exibição de memória é usado para armazenar um contexto gráfico temporário que é trocado pelo contexto de exibição renderizado, *hdc*, para eliminar a cintilação. Implemente a rotina de desenho, que leva os pontos que você armazenou e desenha um círculo nos pontos. O código a seguir mostra como você pode implementar o [**manipulador WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



Quando você executar seu aplicativo, ele agora deverá se parecer com a ilustração no início desta seção.

Para se divertido, você pode desenhar algumas linhas extras em torno dos pontos de toque. A captura de tela a seguir mostra a aparência do aplicativo com algumas linhas extras desenhadas em torno dos círculos.

![captura de tela mostrando um aplicativo que renderiza pontos de toque como círculos com linhas pelos centros e intersecção das bordas dos pontos de toque](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Entrada de toque](guide-multi-touch-input.md)
</dt> </dl>

 

 