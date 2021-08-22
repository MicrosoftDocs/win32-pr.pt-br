---
title: Habilitar e controlar a composição DWM
description: As APIs Gerenciador de Janelas da Área de Trabalho de composição (DWM) fornecem várias funções para definir e consultar informações básicas que são usadas pelo DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), composição
- DWM (Gerenciador de Janelas da Área de Trabalho),composição
- Composição
- composição da área de trabalho
- Colorização
- renderização de região não cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), colorização
- DWM (Gerenciador de Janelas da Área de Trabalho),colorização
- Gerenciador de Janelas da Área de Trabalho (DWM), renderização de região não cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), renderização de região não cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), mensagens
- DWM (Gerenciador de Janelas da Área de Trabalho), mensagens
- mensagens
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: e8c5df1778436e2cfe23df85483453b01fb80884adc9a6d8ff34955deb3e0c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741576"
---
# <a name="enable-and-control-dwm-composition"></a>Habilitar e controlar a composição DWM

As APIs Gerenciador de Janelas da Área de Trabalho de composição (DWM) fornecem várias funções para definir e consultar informações básicas que são usadas pelo DWM. Essas APIs permitem que você consulte e altere o estado da composição. Além disso, você pode definir e consultar a política de renderização para diferentes atributos de janela DWM.

## <a name="retrieving-colorization-information"></a>Recuperando informações de colorização

A cor da região não cliente de uma janela é determinada pelo tema de cor do sistema atual. O valor de colorização é fornecido por meio das APIs DWM para permitir que seu aplicativo corresponder a interface do usuário do cliente com o tema de cor do sistema.

Para acessar esse valor de colorização e monitorar a alteração de cor, use a [**função DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) e a [**mensagem WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) cor.

Este exemplo demonstra como lidar com a mensagem de cor alterada e acessar a nova cor.

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a>Controlando a renderização de região não cliente

Dois dos efeitos visuais que a DWM habilita são a transparência da região não cliente de uma janela e efeitos de transição. Seu aplicativo pode ter que desabilitar ou reabilitar esses efeitos por motivos de estilo ou compatibilidade. As funções a seguir são usadas para gerenciar o comportamento de transparência e efeito de transição.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Para recuperar o estado atual de renderização não cliente para a janela de um aplicativo, chame [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) com *dwAttribute* definido como [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Como você pode ver na documentação do [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), quando você passa esse sinalizador para **DwmGetWindowAttribute**, o valor do atributo recuperado é do tipo **BOOL**. Sinalizadores diferentes fazer **com que DwmGetWindowAttribute** retorne valores de tipos diferentes. Aqui está um exemplo de código.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

Este exemplo a seguir mostra como usar o [**sinalizador DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) com **DwmGetWindowAttribute** para recuperar o retângulo de limites de quadro estendido de uma janela. A documentação desse sinalizador informa que o valor do atributo recuperado é do tipo **RECT.**

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Siga o mesmo padrão de programação mostrado acima quando você chama [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) com sinalizadores para atributos diferentes. O tópico de enumeração [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, na linha de cada sinalizador, para qual tipo de valor você deve passar um ponteiro no parâmetro *pvAttribute* **para DwmGetWindowAttribute**. O *parâmetro cbAttribute* contém o tamanho, em bytes, desse objeto.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) habilita seu aplicativo a definir a política de renderização de área não cliente. Essa função também determina como seu aplicativo deve lidar com efeitos de transição de DWM.

Este exemplo a seguir desabilita a renderização de área não cliente. Isso faz com que todas as chamadas anteriores para [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) ou [para DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) sejam desabilitadas.

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

Além de controlar a renderização de área não cliente, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) também pode controlar efeitos de transição de DWM. Você pode definir o comportamento de transição usando **DWMWA \_ TRANSITIONS \_ FORCEDISABLED** como o *parâmetro dwAttribute.*

## <a name="messages"></a>Mensagens

As mensagens a seguir fornecem notificação de eventos DWM. Essas mensagens podem ser usadas para monitorar alterações, como alterações de estado de composição e alterações de tema de cor do sistema.

- [**WM \_ DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ DWMCOMPOSITIONCHANGED**](wm-dwmcompositionchanged.md)
- [**WM \_ DWMNCRENDERINGCHANGED**](wm-dwmncrenderingchanged.md)
- [**WM \_ DWMWINDOWMAXIMIZEDCHANGE**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows-7-and-earlier"></a>Desabilitando a composição DWM (Windows 7 e versões anteriores)

> [!WARNING]
> As informações nesta seção se aplica somente aos sistemas Windows 7 e anteriores.

Como a DWM usa a GPU (unidade de processamento gráfico) para composição da área de trabalho, seu aplicativo pode ter que desabilitar a DWM para compatibilidade. Os aplicativos que têm controle total da área de trabalho, como jogos executados no modo de tela inteira, devem determinar se a DWM está habilitada e, se estiver, desabilite-a. Para fazer isso, duas funções são necessárias.

- [**Dwmiscompositionenabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Uma chamada para [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) com *fEnable* definido como **DWM \_ EC \_ DISABLECOMPOSITION** desabilita a composição DWM até que o processo de chamada seja desligado ou a composição tenha sido habilitada de novo chamando **DwmEnableComposition** com *fEnable* definido como **DWM \_ EC \_ ENABLECOMPOSITION**. A composição de DWM é reiniciada automaticamente assim que todos os aplicativos que desabilitam a composição foram desligados ou reabilitaram manualmente a composição chamando **DwmEnableComposition.**

> [!NOTE]  
> O DWM desabilita automaticamente a composição quando um aplicativo tenta desenhar diretamente para a superfície de exibição primária. A composição será desabilitada até que a superfície do dispositivo primário seja liberada por esse aplicativo.
