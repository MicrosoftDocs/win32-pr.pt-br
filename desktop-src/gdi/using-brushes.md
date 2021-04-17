---
description: Você pode usar um pincel para pintar o interior de praticamente qualquer forma usando uma função de interface de dispositivo de gráficos (GDI).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Usando pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65ad4b14ba445642f224b0002eb1e7517c1008b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505783"
---
# <a name="using-brushes"></a><span data-ttu-id="e7475-103">Usando pincéis</span><span class="sxs-lookup"><span data-stu-id="e7475-103">Using Brushes</span></span>

<span data-ttu-id="e7475-104">Você pode usar um pincel para pintar o interior de praticamente qualquer forma usando uma função de interface de dispositivo de gráficos (GDI).</span><span class="sxs-lookup"><span data-stu-id="e7475-104">You can use a brush to paint the interior of virtually any shape by using a graphics device interface (GDI) function.</span></span> <span data-ttu-id="e7475-105">Isso inclui os Interiors dos retângulos, das reticências, dos polígonos e dos caminhos.</span><span class="sxs-lookup"><span data-stu-id="e7475-105">This includes the interiors of rectangles, ellipses, polygons, and paths.</span></span> <span data-ttu-id="e7475-106">Dependendo dos requisitos do seu aplicativo, você pode usar um pincel sólido de uma cor especificada, um pincel de ação, um pincel de hachura ou um pincel de padrão.</span><span class="sxs-lookup"><span data-stu-id="e7475-106">Depending on the requirements of your application, you can use a solid brush of a specified color, a stock brush, a hatch brush, or a pattern brush.</span></span>

<span data-ttu-id="e7475-107">Esta seção contém exemplos de código que demonstram a criação de uma caixa de diálogo de pincel personalizada.</span><span class="sxs-lookup"><span data-stu-id="e7475-107">This section contains code samples that demonstrate the creation of a custom brush dialog box.</span></span> <span data-ttu-id="e7475-108">A caixa de diálogo contém uma grade que representa o bitmap que o sistema usa como um pincel.</span><span class="sxs-lookup"><span data-stu-id="e7475-108">The dialog box contains a grid that represents the bitmap the system uses as a brush.</span></span> <span data-ttu-id="e7475-109">Um usuário pode usar essa grade para criar um bitmap de pincel de padrão e, em seguida, exibir o padrão personalizado clicando no botão **padrão de teste** .</span><span class="sxs-lookup"><span data-stu-id="e7475-109">A user can use this grid to create a pattern-brush bitmap and then view the custom pattern by clicking the **Test Pattern** button.</span></span>

<span data-ttu-id="e7475-110">A ilustração a seguir mostra um padrão criado usando a caixa de diálogo **pincel personalizado** .</span><span class="sxs-lookup"><span data-stu-id="e7475-110">The following illustration shows a pattern created by using the **Custom Brush** dialog box.</span></span>

![captura de tela da caixa de diálogo pincel personalizado](images/custbrush.png)

<span data-ttu-id="e7475-112">Para exibir uma caixa de diálogo, primeiro você deve criar um modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e7475-112">To display a dialog box, you must first create a dialog box template.</span></span> <span data-ttu-id="e7475-113">O modelo de caixa de diálogo a seguir define a caixa de diálogo **pincel personalizado** .</span><span class="sxs-lookup"><span data-stu-id="e7475-113">The following dialog box template defines the **Custom Brush** dialog box.</span></span>


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



<span data-ttu-id="e7475-114">A caixa de diálogo **pincel personalizado** contém cinco controles: uma janela de grade de bitmap, uma janela de exibição de padrão e três botões de push, o **padrão de teste** rotulado, **OK** e **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="e7475-114">The **Custom Brush** dialog box contains five controls: a bitmap-grid window, a pattern-viewing window, and three push buttons, labeled **Test Pattern**, **OK**, and **Cancel**.</span></span> <span data-ttu-id="e7475-115">O botão de ação de **padrão de teste** permite que o usuário exiba o padrão.</span><span class="sxs-lookup"><span data-stu-id="e7475-115">The **Test Pattern** push button enables the user to view the pattern.</span></span> <span data-ttu-id="e7475-116">O modelo da caixa de diálogo especifica as dimensões gerais da janela da caixa de diálogo, atribui um valor a cada controle, especifica o local de cada controle e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e7475-116">The dialog box template specifies the overall dimensions of the dialog box window, assigns a value to each control, specifies the location of each control, and so forth.</span></span> <span data-ttu-id="e7475-117">Para obter mais informações, consulte [caixas de diálogo](../dlgbox/dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="e7475-117">For more information, see [Dialog Boxes](../dlgbox/dialog-boxes.md).</span></span>

<span data-ttu-id="e7475-118">Os valores de controle no modelo da caixa de diálogo são constantes que foram definidas da seguinte maneira no arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7475-118">The control values in the dialog box template are constants that have been defined as follows in the application's header file.</span></span>


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



<span data-ttu-id="e7475-119">Depois de criar um modelo de caixa de diálogo e incluí-lo no arquivo de definição de recurso do aplicativo, você deve escrever um procedimento de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e7475-119">After you create a dialog box template and include it in the application's resource-definition file, you must write a dialog procedure.</span></span> <span data-ttu-id="e7475-120">Esse procedimento processa as mensagens que o sistema envia para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e7475-120">This procedure processes messages that the system sends to the dialog box.</span></span> <span data-ttu-id="e7475-121">O trecho a seguir do código-fonte de um aplicativo mostra o procedimento da caixa de diálogo para a caixa de diálogo **pincel personalizado** e as duas funções definidas pelo aplicativo que ele chama.</span><span class="sxs-lookup"><span data-stu-id="e7475-121">The following excerpt from an application's source code shows the dialog box procedure for the **Custom Brush** dialog box and the two application-defined functions it calls.</span></span>


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



<span data-ttu-id="e7475-122">O procedimento da caixa de diálogo para a caixa de diálogo **pincel personalizado** processa quatro mensagens, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7475-122">The dialog box procedure for the **Custom Brush** dialog box processes four messages, as described in the following table.</span></span>



| <span data-ttu-id="e7475-123">Mensagem</span><span class="sxs-lookup"><span data-stu-id="e7475-123">Message</span></span>                                          | <span data-ttu-id="e7475-124">Ação</span><span class="sxs-lookup"><span data-stu-id="e7475-124">Action</span></span>                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7475-125">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7475-125">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)   | <span data-ttu-id="e7475-126">Recupera um identificador de janela e dimensões para os controles da janela de grade e do pincel de padrão, computa as dimensões de uma única célula no controle de janela de grade e Inicializa uma matriz de coordenadas de célula de grade.</span><span class="sxs-lookup"><span data-stu-id="e7475-126">Retrieves a window handle and dimensions for the grid-window and pattern-brush controls, computes the dimensions of a single cell in the grid-window control, and initializes an array of grid-cell coordinates.</span></span>                                                                                           |
| [<span data-ttu-id="e7475-127">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7475-127">**WM\_PAINT**</span></span>](wm-paint.md)                    | <span data-ttu-id="e7475-128">Desenha o padrão de grade no controle da janela de grade.</span><span class="sxs-lookup"><span data-stu-id="e7475-128">Draws the grid pattern in the grid-window control.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e7475-129">**LBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7475-129">**WM\_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md) | <span data-ttu-id="e7475-130">Determina se o cursor está dentro do controle da janela de grade quando o usuário pressiona o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="e7475-130">Determines whether the cursor is within the grid-window control when the user presses the left mouse button.</span></span> <span data-ttu-id="e7475-131">Nesse caso, o procedimento da caixa de diálogo inverte a célula de grade apropriada e registra o estado dessa célula em uma matriz de bits que é usada para criar o bitmap para o pincel personalizado.</span><span class="sxs-lookup"><span data-stu-id="e7475-131">If so, the dialog box procedure inverts the appropriate grid cell and records the state of that cell in an array of bits that is used to create the bitmap for the custom brush.</span></span>              |
| [<span data-ttu-id="e7475-132">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7475-132">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)         | <span data-ttu-id="e7475-133">Processa a entrada para os três controles de botão de ação.</span><span class="sxs-lookup"><span data-stu-id="e7475-133">Processes input for the three push button controls.</span></span> <span data-ttu-id="e7475-134">Se o usuário clicar no botão de **padrão de teste** , o procedimento da caixa de diálogo pintará o controle de padrão de teste com o novo padrão de pincel personalizado.</span><span class="sxs-lookup"><span data-stu-id="e7475-134">If the user clicks the **Test Pattern** button, the dialog box procedure paints the Test Pattern control with the new custom brush pattern.</span></span> <span data-ttu-id="e7475-135">Se o usuário clicar no botão **OK** ou **Cancelar** , o procedimento da caixa de diálogo executará as ações adequadamente.</span><span class="sxs-lookup"><span data-stu-id="e7475-135">If the user clicks the **OK** or **Cancel** button, the dialog box procedure performs actions accordingly.</span></span> |



 

<span data-ttu-id="e7475-136">Para obter mais informações sobre mensagens e processamento de mensagem, consulte [mensagens e filas](../winmsg/messages-and-message-queues.md)de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e7475-136">For more information about messages and message processing, see [Messages and Message Queues](../winmsg/messages-and-message-queues.md).</span></span>

<span data-ttu-id="e7475-137">Depois de escrever o procedimento da caixa de diálogo, inclua a definição da função para o procedimento no arquivo de cabeçalho do aplicativo e, em seguida, chame o procedimento da caixa de diálogo no ponto apropriado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7475-137">After you write the dialog box procedure, include the function definition for the procedure in the application's header file and then call the dialog box procedure at the appropriate point in the application.</span></span>

<span data-ttu-id="e7475-138">O trecho a seguir do arquivo de cabeçalho do aplicativo mostra a definição da função para o procedimento da caixa de diálogo e as duas funções que ele chama.</span><span class="sxs-lookup"><span data-stu-id="e7475-138">The following excerpt from the application's header file shows the function definition for the dialog box procedure and the two functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



<span data-ttu-id="e7475-139">Por fim, o código a seguir mostra como o procedimento da caixa de diálogo é chamado a partir do arquivo de código-fonte do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7475-139">Finally, the following code shows how the dialog box procedure is called from the application's source-code file.</span></span>


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



<span data-ttu-id="e7475-140">Normalmente, essa chamada é feita em resposta ao usuário que escolhe uma opção no menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7475-140">This call is usually made in response to the user choosing an option from the application's menu.</span></span>

 

 
