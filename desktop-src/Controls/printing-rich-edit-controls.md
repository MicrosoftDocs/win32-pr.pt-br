---
title: Como imprimir o conteúdo de controles de edição rich
description: Esta seção contém informações sobre como imprimir o conteúdo de controles de edição rich.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00c7a7287fc86e47e085cfacd7757a7e24b4a91a3a513e75dc4610b51606b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575546"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Como imprimir o conteúdo de controles de edição rich

Esta seção contém informações sobre como imprimir o conteúdo de controles de edição rich.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-print-preview"></a>Usar a visualização de impressão

Para formatar texto em um controle de edição rico, pois ele aparecerá em um dispositivo de destino (geralmente a página impressa), envie a mensagem [**EM \_ SETTARGETDEVICE,**](em-settargetdevice.md) passando o handle para um HDC (contexto de dispositivo) do dispositivo de destino e a largura de linha desejada. Normalmente, você obterá a largura da linha chamando [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para o HDC de destino.

### <a name="format-print-for-a-specific-device"></a>Formatar impressão para um dispositivo específico

Para formatar parte do conteúdo de um controle de edição rich para um dispositivo específico, envie a [**mensagem EM \_ FORMATRANGE.**](em-formatrange.md) A [**estrutura FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) usada com essa mensagem especifica o intervalo de texto a ser formatado, bem como o HDC para o dispositivo de destino. Opcionalmente, essa mensagem também envia o texto para a impressora.

### <a name="use-banding"></a>Usar o banding

A banda é o processo pelo qual uma única página de saída é gerada usando um ou mais retângulos separados ou faixas. Quando todas as faixas são colocadas na página, uma imagem completa resulta. Essa abordagem geralmente é usada por impressoras raster que não têm memória suficiente ou capacidade de criar uma imagem de uma página inteira ao mesmo tempo.

Para implementar a banda, use a [**mensagem EM \_ DISPLAYBAND**](em-displayband.md) para enviar partes sucessivas do conteúdo do controle de edição rich para o dispositivo. Essa mensagem imprime no dispositivo que foi especificado em uma chamada anterior para [**EM \_ FORMATRANGE.**](em-formatrange.md) É claro que o *parâmetro wParam* da mensagem **EM \_ FORMATRANGE** deve ser zero, de modo que a impressão não seja iniciada por essa mensagem.

## <a name="printrtf-code-example"></a>Exemplo de código PrintRTF

O código de exemplo a seguir imprime o conteúdo de um controle de edição rico na impressora especificada.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 