---
title: Habilitar e controlar a composição do DWM
description: As APIs de composição do Gerenciador de Janelas da Área de Trabalho (DWM) fornecem várias funções para configurar e consultar informações básicas que são usadas pelo DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), composição
- DWM (Gerenciador de Janelas da Área de Trabalho), composição
- composição
- composição de área de trabalho
- colorização
- renderização de região não cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), colorização
- DWM (Gerenciador de Janelas da Área de Trabalho), colorização
- Gerenciador de Janelas da Área de Trabalho (DWM), renderização de região não cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), renderização de região não cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), mensagens
- DWM (Gerenciador de Janelas da Área de Trabalho), mensagens
- mensagens
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822940"
---
# <a name="enable-and-control-dwm-composition"></a>Habilitar e controlar a composição do DWM

As APIs de composição do Gerenciador de Janelas da Área de Trabalho (DWM) fornecem várias funções para configurar e consultar informações básicas que são usadas pelo DWM. Essas APIs permitem consultar e alterar o estado de composição. Além disso, você pode definir e consultar a política de renderização para diferentes atributos de janela do DWM.

## <a name="retrieving-colorization-information"></a>Recuperando informações de colorização

A cor da região não cliente de uma janela é determinada pelo tema de cores do sistema atual. O valor de colorização é fornecido por meio das APIs do DWM para permitir que seu aplicativo corresponda a interface do usuário do cliente com o tema de cores do sistema.

Para acessar esse valor de colorização e monitorar a alteração de cor, use a função [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) e a mensagem de [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .

Este exemplo demonstra como manipular a mensagem de alteração de cor e acessar a nova cor.

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

Dois dos efeitos visuais que o DWM permite são transparências da região não cliente de uma janela e efeitos de transição. Seu aplicativo pode ter que desabilitar ou reabilitar esses efeitos para estilos ou motivos de compatibilidade. As funções a seguir são usadas para gerenciar o comportamento de efeito de transição e transparência.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Para recuperar o estado de renderização não cliente atual para a janela de um aplicativo, chame [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) com *dwAttribute* definido como [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Como você pode ver na documentação para [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), quando você passa esse sinalizador para **DwmGetWindowAttribute**, o valor do atributo recuperado é do tipo **bool**. Sinalizadores diferentes fazem com que o **DwmGetWindowAttribute** retorne valores de tipos diferentes. Aqui está um exemplo de código.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

Este exemplo a seguir mostra como usar o sinalizador [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) com **DwmGetWindowAttribute** para recuperar o retângulo de limites de quadro estendido de uma janela. A documentação para esse sinalizador nos informa que o valor do atributo recuperado é do tipo **Rect**.

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Siga o mesmo padrão de programação mostrado acima ao chamar [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) com sinalizadores para atributos diferentes. O tópico de enumeração [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, na linha para cada sinalizador, a qual tipo de valor você deve passar um ponteiro no parâmetro *pvAttribute* para **DwmGetWindowAttribute**. O parâmetro *cbAttribute* contém o tamanho, em bytes, desse objeto.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) permite que seu aplicativo defina a política de renderização de área não cliente. Essa função também determina como seu aplicativo deve tratar os efeitos de transição do DWM.

Este próximo exemplo desabilita a renderização de área que não é do cliente. Isso faz com que todas as chamadas anteriores para [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) ou [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) sejam desabilitadas.

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

Além de controlar a renderização de área de não cliente, o [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) também pode controlar os efeitos de transição do DWM. Você pode definir o comportamento de transição **usando \_ transições DWMWA \_ FORCEDISABLED** como o parâmetro *dwAttribute* .

## <a name="messages"></a>Mensagens

As mensagens a seguir fornecem notificação de eventos do DWM. Essas mensagens podem ser usadas para monitorar alterações, como alterações de estado de composição e alterações de tema de cores do sistema.

- [**DWMCOLORIZATIONCOLORCHANGED do WM \_**](wm-dwmcolorizationcolorchanged.md)
- [**DWMCOMPOSITIONCHANGED do WM \_**](wm-dwmcompositionchanged.md)
- [**DWMNCRENDERINGCHANGED do WM \_**](wm-dwmncrenderingchanged.md)
- [**DWMWINDOWMAXIMIZEDCHANGE do WM \_**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a>Desabilitando a composição do DWM (Windows 7 e anterior)

> [!WARNING]
> As informações nesta seção aplicam-se somente ao Windows 7 e aos sistemas anteriores.

Como o DWM usa a GPU (unidade de processamento gráfico) para composição de área de trabalho, seu aplicativo pode ter que desabilitar o DWM para compatibilidade. Os aplicativos que assumem controle total da área de trabalho, como jogos executados no modo de tela inteira, devem determinar se o DWM está habilitado e, se estiver, desabilitá-lo. Para fazer isso, são necessárias duas funções.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Uma chamada para [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) com *FEnable* definido como **DWM \_ EC \_ DISABLECOMPOSITION** desabilita a composição do DWM até que o processo de chamada tenha sido desligado ou a composição tenha sido reabilitada chamando **DwmEnableComposition** com *fEnable* definido como **DWM \_ EC \_ ENABLECOMPOSITION**. A composição do DWM é reiniciada automaticamente assim que todos os aplicativos que têm a composição desabilitada são desligados ou reativados manualmente por meio da chamada de **DwmEnableComposition**.

> [!NOTE]  
> O DWM desabilita automaticamente a composição quando um aplicativo tenta desenhar diretamente na superfície de exibição primária. A composição será desabilitada até que a superfície do dispositivo primário seja liberada por esse aplicativo.
