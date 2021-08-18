---
description: Você pode usar um pincel para pintar o interior de praticamente qualquer forma usando uma função de GDI (interface de dispositivo gráfico).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Usando pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42e09dc5731ceba7961dfd66b296df531897f2915cff53ccdacf1b5b5740160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037494"
---
# <a name="using-brushes"></a>Usando pincéis

Você pode usar um pincel para pintar o interior de praticamente qualquer forma usando uma função de GDI (interface de dispositivo gráfico). Isso inclui os interiores de retângulos, reellipses, polígonos e caminhos. Dependendo dos requisitos do seu aplicativo, você pode usar um pincel sólido de uma cor especificada, um pincel de estoque, um pincel de hatch ou um pincel de padrão.

Esta seção contém exemplos de código que demonstram a criação de uma caixa de diálogo de pincel personalizada. A caixa de diálogo contém uma grade que representa o bitmap que o sistema usa como um pincel. Um usuário pode usar essa grade para criar um bitmap de pincel padrão e, em seguida, exibir o padrão personalizado clicando no **botão Padrão de** Teste.

A ilustração a seguir mostra um padrão criado usando a **caixa de diálogo Pincel** Personalizado .

![captura de tela da caixa de diálogo pincel personalizado](images/custbrush.png)

Para exibir uma caixa de diálogo, você deve primeiro criar um modelo de caixa de diálogo. O modelo de caixa de diálogo a seguir define a **caixa de diálogo Pincel** Personalizado.


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



A **caixa de** diálogo Pincel Personalizado contém cinco controles: uma janela de grade bitmap, uma janela de exibição de padrões e três botões de push, rotulados Padrão de Teste , **OK** e **Cancelar**.  O **botão de** push Padrão de Teste permite que o usuário veja o padrão. O modelo de caixa de diálogo especifica as dimensões gerais da janela da caixa de diálogo, atribui um valor a cada controle, especifica o local de cada controle e assim por diante. Para obter mais informações, consulte [Caixas de diálogo](../dlgbox/dialog-boxes.md).

Os valores de controle no modelo de caixa de diálogo são constantes que foram definidas da seguinte forma no arquivo de header do aplicativo.


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



Depois de criar um modelo de caixa de diálogo e incluí-lo no arquivo de definição de recursos do aplicativo, você deve escrever um procedimento de caixa de diálogo. Esse procedimento processa mensagens que o sistema envia para a caixa de diálogo. O trecho a seguir do código-fonte de um aplicativo  mostra o procedimento da caixa de diálogo para a caixa de diálogo Pincel Personalizado e as duas funções definidas pelo aplicativo que ele chama.


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



O procedimento da caixa de diálogo para **a caixa de** diálogo Pincel Personalizado processa quatro mensagens, conforme descrito na tabela a seguir.



| Mensagem                                          | Ação                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)   | Recupera uma alça de janela e dimensões para os controles de janela de grade e de pincel padrão, calcula as dimensões de uma única célula no controle de janela de grade e inicializa uma matriz de coordenadas de célula de grade.                                                                                           |
| [**WM \_ PAINT**](wm-paint.md)                    | Desenha o padrão de grade no controle de janela de grade.                                                                                                                                                                                                                                                         |
| [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) | Determina se o cursor está dentro do controle de janela de grade quando o usuário pressiona o botão esquerdo do mouse. Nesse caso, o procedimento da caixa de diálogo inverte a célula de grade apropriada e registra o estado dessa célula em uma matriz de bits que é usada para criar o bitmap para o pincel personalizado.              |
| [**COMANDO \_ WM**](../menurc/wm-command.md)         | Processa a entrada para os três controles de botão de push. Se o usuário clicar no botão **Padrão de** Teste, o procedimento da caixa de diálogo pintará o controle Padrão de Teste com o novo padrão de pincel personalizado. Se o usuário clicar no **botão OK** ou **Cancelar,** o procedimento da caixa de diálogo executará ações de acordo. |



 

Para obter mais informações sobre mensagens e processamento de mensagens, consulte [Mensagens e filas de mensagens](../winmsg/messages-and-message-queues.md).

Depois de gravar o procedimento da caixa de diálogo, inclua a definição de função para o procedimento no arquivo de header do aplicativo e, em seguida, chame o procedimento da caixa de diálogo no ponto apropriado no aplicativo.

O trecho a seguir do arquivo de header do aplicativo mostra a definição de função para o procedimento da caixa de diálogo e as duas funções que ele chama.


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



Por fim, o código a seguir mostra como o procedimento da caixa de diálogo é chamado do arquivo de código-fonte do aplicativo.


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



Essa chamada geralmente é feita em resposta ao usuário escolhendo uma opção no menu do aplicativo.

 

 
