---
title: Como imprimir o conteúdo de controles de edição avançados
description: Esta seção contém informações sobre como imprimir o conteúdo de controles de edição avançados.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105753570"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="45715-103">Como imprimir o conteúdo de controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="45715-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="45715-104">Esta seção contém informações sobre como imprimir o conteúdo de controles de edição avançados.</span><span class="sxs-lookup"><span data-stu-id="45715-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="45715-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="45715-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="45715-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="45715-106">Technologies</span></span>

-   [<span data-ttu-id="45715-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="45715-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="45715-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="45715-108">Prerequisites</span></span>

-   <span data-ttu-id="45715-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="45715-109">C/C++</span></span>
-   <span data-ttu-id="45715-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="45715-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="45715-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="45715-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="45715-112">Usar visualização de impressão</span><span class="sxs-lookup"><span data-stu-id="45715-112">Use Print Preview</span></span>

<span data-ttu-id="45715-113">Para formatar o texto em um controle de edição rico, como ele aparecerá em um dispositivo de destino (geralmente, a página impressa), envie a mensagem em [**\_ SETTARGETDEVICE**](em-settargetdevice.md) , passando o identificador para um contexto de dispositivo (HDC) do dispositivo de destino e a largura de linha desejada.</span><span class="sxs-lookup"><span data-stu-id="45715-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="45715-114">Normalmente, você obterá a largura da linha chamando [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para o HDC de destino.</span><span class="sxs-lookup"><span data-stu-id="45715-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="45715-115">Formato de impressão para um dispositivo específico</span><span class="sxs-lookup"><span data-stu-id="45715-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="45715-116">Para formatar parte de um conteúdo de controle de edição rico para um dispositivo específico, envie a mensagem em [**\_ FORMATRANGE**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="45715-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="45715-117">A estrutura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) usada com essa mensagem Especifica o intervalo de texto a ser formatado, bem como o HDC para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="45715-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="45715-118">Opcionalmente, essa mensagem também envia o texto para a impressora.</span><span class="sxs-lookup"><span data-stu-id="45715-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="45715-119">Usar faixa</span><span class="sxs-lookup"><span data-stu-id="45715-119">Use Banding</span></span>

<span data-ttu-id="45715-120">A faixa é o processo pelo qual uma única página de saída é gerada usando um ou mais retângulos ou faixas separadas.</span><span class="sxs-lookup"><span data-stu-id="45715-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="45715-121">Quando todas as faixas são colocadas na página, uma imagem completa resulta.</span><span class="sxs-lookup"><span data-stu-id="45715-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="45715-122">Essa abordagem é geralmente usada por impressoras rasterizadas que não têm memória suficiente ou capacidade de fazer a imagem de uma página inteira ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="45715-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="45715-123">Para implementar a faixa, use a mensagem em [**\_ DISPLAYBAND**](em-displayband.md) para enviar partes sucessivas do conteúdo do controle de edição rico para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45715-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="45715-124">Essa mensagem é impressa no dispositivo que foi especificado em uma chamada anterior para [**em \_ FORMATRANGE**](em-formatrange.md).</span><span class="sxs-lookup"><span data-stu-id="45715-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="45715-125">É claro que o parâmetro *wParam* da mensagem **em \_ FORMATRANGE** deve ser zero, de modo que a impressão não seja iniciada por essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="45715-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="45715-126">Exemplo de código PrintRTF</span><span class="sxs-lookup"><span data-stu-id="45715-126">PrintRTF Code Example</span></span>

<span data-ttu-id="45715-127">O código de exemplo a seguir imprime o conteúdo de um controle rich edit para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="45715-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="45715-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45715-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45715-129">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="45715-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="45715-130">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="45715-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 