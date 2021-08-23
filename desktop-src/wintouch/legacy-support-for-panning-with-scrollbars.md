---
title: Suporte herdado para movimento panorâmico com barras de rolagem
description: esta seção descreve o suporte para movimento panorâmico usando barras de rolagem em aplicativos baseados em Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Toque, suporte herdado
- movimento panorâmico com barras de rolagem
- Windows Toque, movimento panorâmico com barras de rolagem
- Windows Toque, barras de rolagem
- barras de rolagem, panorâmica
- barras de rolagem, suporte herdado
- Windows Toque, gestos
- gestos, movimento panorâmico com barras de rolagem
- Windows Toque, movimentos
- movimentos, panorâmicas com barras de rolagem
- movimentos, desabilitando
- Windows Toque, mensagens de roda do mouse
- mensagens de roda do mouse
- Windows Toque, personalizando a panorâmica
- panorâmica, barras de rolagem
- visão panorâmica, suporte herdado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97190d637cae5cc6936ecd78dca31e1e6c0f9ef1037b292b6080f973fc4e8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086293"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Suporte herdado para movimento panorâmico com barras de rolagem

esta seção descreve o suporte para movimento panorâmico usando barras de rolagem em aplicativos baseados em Windows.

no Windows 7, gestos de panorâmica geram \_ \* mensagens de rolagem do WM para habilitar o suporte herdado para movimento panorâmico. Como seus aplicativos podem não dar suporte a todas as \_ \* mensagens de rolagem do WM, o movimento panorâmico pode não funcionar corretamente. Este tópico descreve as etapas que você deve seguir para garantir que a experiência de panorâmica herdada em aplicativos funcione conforme os usuários esperam.

## <a name="overview"></a>Visão geral

As seções a seguir explicam como habilitar a experiência de panorâmica herdada:

-   Crie um aplicativo com barras de rolagem.
-   Desabilitar movimentos.
-   Personalize a experiência de panorâmica.

## <a name="create-an-application-with-scroll-bars"></a>Criar um aplicativo com barras de rolagem

inicie um novo projeto Win32 usando o assistente de Microsoft Visual Studio. verifique se o tipo de aplicativo está definido como o Windows aplicativo. Você não precisa habilitar o suporte para o Active Template Library (ATL). A imagem a seguir mostra qual será a aparência do seu projeto depois de você iniciá-lo.

![captura de tela mostrando uma janela sem barras de rolagem](images/gpd-1.png)

Em seguida, habilite as barras de rolagem na imagem. Altere o código de criação da janela em **InitInstance** para que a chamada de função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crie uma janela com barras de rolagem. O código a seguir mostra como fazer isso.


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



Depois de alterar o código de criação da janela, seu aplicativo terá uma barra de rolagem. A imagem a seguir mostra como o aplicativo pode parecer com esse ponto.

![captura de tela mostrando uma janela com uma barra de rolagem vertical, mas sem texto](images/gpd-2.png)

Depois de alterar o código de criação da janela, adicione um objeto de barra de rolagem ao seu aplicativo e algum texto para rolar. Coloque o código a seguir na parte superior do método **WndProc** .


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



Em seguida, implemente a lógica do aplicativo para configurar os cálculos de texto para métricas de texto. O código a seguir deve substituir o caso de **\_ criação** existente do WM na função **WndProc** .


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



Em seguida, implemente a lógica do aplicativo para recálculo do bloco de texto quando a janela for redimensionada. O código a seguir deve ser colocado na chave de mensagem em **WndProc**.


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



Em seguida, implemente a lógica do aplicativo para mensagens de rolagem vertical. O código a seguir deve ser colocado na chave de mensagem em **WndProc**.


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



Em seguida, atualize o código para redesenhar a janela. O código a seguir deve substituir o caso de **\_ pintura** padrão do WM em **WndProc**.


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



Agora, quando você cria e executa seu aplicativo, ele deve ter o texto clichê e uma barra de rolagem vertical. A imagem a seguir mostra como o seu aplicativo pode parecer.

![captura de tela mostrando uma janela com uma barra de rolagem vertical e texto](images/gpd-3.png)

## <a name="disable-flicks"></a>Desabilitar movimentos

Para melhorar a experiência de panorâmica em seu aplicativo, você deve desligar os movimentos. Para fazer isso, defina as propriedades da janela no valor de *HWND* quando ele for inicializado. Os valores usados para movimentos são armazenados no cabeçalho tpcshrd. h, que também deve ser incluído. O código a seguir deve ser colocado em suas diretivas include e na função **InitInstance** depois de você ter criado o *HWND*.

> [!Note]  
> Isso é útil para aplicativos que exigem comentários imediatos sobre um evento de toque ou caneta, em vez de testar por um limite de tempo ou de distância.

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a>Personalizar a experiência de panorâmica

você pode querer uma experiência de panorâmica diferente da oferecida pelo Windows 7 por padrão. Para melhorar a experiência de panorâmica, você deve adicionar o manipulador para a mensagem de [**\_ gesto do WM**](wm-gesture.md) . Para obter mais informações, consulte [aprimorando a experiência de panorâmica Single-Finger](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Gestos de toque](guide-multi-touch-gestures.md)
</dt> </dl>

 

 