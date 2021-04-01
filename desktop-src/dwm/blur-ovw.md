---
title: Desfoque do DWM por trás da visão geral
description: Um dos efeitos de Gerenciador de Janelas da Área de Trabalho de assinatura (DWM) é uma área de não-cliente translúcida e borrada. As APIs do DWM permitem que os aplicativos apliquem esses efeitos à área do cliente de suas janelas de nível superior.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), efeito desfoque-atrás
- DWM (Gerenciador de Janelas da Área de Trabalho), efeito desfoque-atrás
- efeito borrar-atrás
- efeito translúcida
- efeito de vidro transparente
- Gerenciador de Janelas da Área de Trabalho (DWM), efeito translúcida
- DWM (Gerenciador de Janelas da Área de Trabalho), efeito translúcida
- Gerenciador de Janelas da Área de Trabalho (DWM), efeito de vidro transparente
- DWM (Gerenciador de Janelas da Área de Trabalho), efeito de vidro transparente
- Gerenciador de Janelas da Área de Trabalho (DWM), estendendo o quadro da janela na área do cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), estendendo o quadro de janela na área do cliente
- estendendo o quadro da janela na área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008063"
---
# <a name="dwm-blur-behind-overview"></a>Desfoque do DWM por trás da visão geral

Um dos efeitos de Gerenciador de Janelas da Área de Trabalho de assinatura (DWM) é uma área de não-cliente translúcida e borrada. As APIs do DWM permitem que os aplicativos apliquem esses efeitos à área do cliente de suas janelas de nível superior.

> [!Note]  
> O Windows Vista Home Basic Edition não dá suporte ao efeito de vidro transparente. As áreas que normalmente renderizariam com o efeito de vidro transparente em outras edições do Windows são renderizadas como opacas.
> A partir do Windows 8, chamar essa função não resulta no efeito de desfoque, devido a uma alteração de estilo na maneira como as janelas são renderizadas.


 

Este tópico discute os seguintes cenários de desfoque do cliente que o DWM habilita.

-   [Adicionando desfoque a uma região específica da área do cliente](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Estendendo o quadro da janela para a área do cliente](#extending-the-window-frame-into-the-client-area)
-   [Tópicos relacionados](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Adicionando desfoque a uma região específica da área do cliente

Um aplicativo pode aplicar o efeito de desfoque atrás de toda a região do cliente da janela ou de uma sub-região específica. Isso permite que os aplicativos adicionem um caminho com estilo e barras de pesquisa que são visualmente separadas do restante do aplicativo.

A API usada neste cenário é a função [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , que usa o [**DWM Blur por trás das constantes**](dwm-bb-constants.md) e a estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .

A função de exemplo a seguir, `EnableBlurBehind` , ilustra como aplicar o efeito desfoque-atrás à janela inteira.


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Observe que **NULL** é especificado no parâmetro *hRgnBlur* . Isso informa ao DWM para aplicar o desfoque por trás de toda a janela.

A imagem a seguir ilustra o efeito desfoque-atrás aplicado à janela inteira.

![o efeito de desfoque aplicado a uma janela](images/dwm-blurbehindwindow.png)

Para aplicar o desfoque por trás de uma subregião, aplique um identificador de região válido (HRGN) ao membro **hRgnBlur** da estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) e adicione o sinalizador **DWM \_ BB \_ BLURREGION** ao membro **dwFlags** .

Quando você aplica o efeito desfoque-atrás a uma subregião da janela, o canal alfa da janela é usado para a área não borrada. Isso pode causar uma transparência inesperada na região não borrada de uma janela. Portanto, tenha cuidado ao aplicar um efeito de desfoque a uma sub-região.

## <a name="extending-the-window-frame-into-the-client-area"></a>Estendendo o quadro da janela para a área do cliente

Um aplicativo pode estender o desfoque do quadro da janela para a área do cliente. Isso é útil quando você aplica o efeito de desfoque por trás de uma janela com uma barra de ferramentas encaixada ou separa visualmente os controles do restante de um aplicativo. Essa funcionalidade é exposta pela função [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

Para habilitar o desfoque usando [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use a estrutura [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) para indicar quanto estender para a área do cliente. A função de exemplo a seguir, `ExtendIntoClientBottom` , alterna a extensão de desfoque na parte inferior do quadro de não cliente para a área do cliente.


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



A imagem a seguir ilustra o efeito de desfoque estendido na parte inferior da área do cliente.

![imagem que mostra o efeito de desfoque estendido na parte inferior de uma área do cliente](images/dwm-extendedbottom.png)

Também está disponível por meio do método [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) , o efeito de "folha de vidro", em que o efeito de desfoque é aplicado à superfície inteira da janela sem uma borda de janela visível. O exemplo a seguir demonstra esse efeito em que a área do cliente é renderizada sem uma borda de janela.


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



A imagem a seguir ilustra o desfoque no estilo de janela "folha de vidro".

![imagem que ilustra o efeito desfoque-atrás no estilo de janela "folha de vidro"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Gerenciador de Janelas da Área de Trabalho](dwm-overview.md)
</dt> <dt>

[Habilitar e controlar a composição do DWM](composition-ovw.md)
</dt> <dt>

[Considerações sobre desempenho e práticas recomendadas](bestpractices-ovw.md)
</dt> </dl>

 

 