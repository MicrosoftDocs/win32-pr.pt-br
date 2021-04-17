---
title: Considerações sobre desempenho e práticas recomendadas
description: Este tópico apresenta um conjunto de práticas recomendadas para usar as APIs do Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), práticas recomendadas
- DWM (Gerenciador de Janelas da Área de Trabalho), práticas recomendadas
- Gerenciador de Janelas da Área de Trabalho (DWM), práticas de aplicativo
- DWM (Gerenciador de Janelas da Área de Trabalho), práticas de aplicativo
- Gerenciador de Janelas da Área de Trabalho (DWM), práticas de desenho
- DWM (Gerenciador de Janelas da Área de Trabalho), práticas de desenho
- Gerenciador de Janelas da Área de Trabalho (DWM), Desfoque atrás do efeito
- DWM (Gerenciador de Janelas da Área de Trabalho), Desfoque atrás do efeito
- práticas de aplicativo
- práticas de desenho
- desfoque atrás do efeito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec76a4920a91f9502940e866d58641a2550d9354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782687"
---
# <a name="performance-considerations-and-best-practices"></a>Considerações sobre desempenho e práticas recomendadas

Este tópico apresenta um conjunto de práticas recomendadas para usar as APIs do Gerenciador de Janelas da Área de Trabalho (DWM).

Este tópico contém as seguintes seções:

-   [Práticas de aplicativo para DWM](#application-practices-for-dwm)
-   [Práticas de desenho para DWM](#drawing-practices-for-dwm)
-   [Blur-Behind de região do cliente do DWM](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Práticas de aplicativo para DWM

Se o seu aplicativo lida com o dimensionamento de pontos por polegada (DPI), você pode declarar um aplicativo como reconhecimento de dpi e impedir o dimensionamento automático definindo o sinalizador de reconhecimento de dpi no manifesto do programa ou chamando a função [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) durante a inicialização do programa.

Com a composição do DWM ativada, os aplicativos obscuros não recebem mais mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e não são solicitados a renderizar novamente. O conteúdo de cada janela já está disponível para compor a imagem da tela.

As janelas [**\_ \_ transparentes do WS ex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) de nível superior devem ser combinadas com um estilo de **\_ \_ camada WS ex** para fins de teste de clique. **WS \_ Por exemplo, \_ transparente** no sentido clássico, sem redirecionamento, é útil para janelas filhas em uma hierarquia de janelas que pertencem ao mesmo thread, mas não se destina a janelas de nível superior.

Use regiões ou camadas para criar janelas moldadas ou mistas. Observe que no Windows Vista e versões posteriores do Windows, o desenho personalizado apenas parte de uma janela de nível superior não fornecerá o conteúdo obsoleto desejado em regiões não desempates.

APIs como [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) podem ser usadas para determinar determinados valores reais. Se você tiver um DC (contexto de dispositivo) para uma janela redirecionada, a origem retornada por **GetDCOrgEx** não corresponderá à origem da janela na tela. Em vez disso, a origem será a origem da superfície do buffer de fundo para sua janela: (0,0).

Quando todo o resto falhar, desabilite a renderização da janela chamando a função [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) .

## <a name="drawing-practices-for-dwm"></a>Práticas de desenho para DWM

Evite desenhar diretamente na superfície de exibição primária. Isso forçará o DWM a desabilitar a composição até que seu aplicativo libere a superfície do dispositivo primário.

Avalie se seu aplicativo deve fornecer seu próprio buffer duplo. O DWM efetivamente armazena em buffer duplo o conteúdo e apresenta a janela em um único quadro.

Evite ler ou gravar em um controlador de domínio de vídeo. Embora tenha suporte do DWM, não recomendamos isso devido a um desempenho reduzido.

Evite desenhar na área não cliente. Embora essa área possa ser acessada pelo aplicativo e o desenho tenha suporte da API do Microsoft Win32, fazer isso pode fazer com que a janela perca qualquer borda de vidro.

Evite misturar o Windows Graphics Device Interface (GDI) e o Microsoft DirectX, a menos que eles não se sobreponham. Se a combinação for necessária, desenhe o conteúdo GDI em uma superfície de software do DirectX e combine-o antes de redigir na tela, ou então desenhe-os em janelas separadas.

Use a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) ou [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) em vez do Windows GDI+ para apresentar o desenho para renderização. O GDI+ renderiza uma linha de varredura por vez com a renderização de software. Isso pode causar oscilação em seus aplicativos.

## <a name="dwm-blur-behind-client-region"></a>Blur-Behind de região do cliente do DWM

A renderização do efeito de desfoque é uma operação com uso intensivo de recursos para a CPU e a GPU (unidade de processamento gráfico). Os desenvolvedores de aplicativos são incentivados a considerar as implicações de usar o desfoque da área do cliente para que ele não consuma recursos excessivos. Você deve usar cuidado especial nos seguintes casos:

-   Quando você espera que o tamanho do desfoque da área do cliente seja significativo, mesmo que nenhuma atualização ocorra na área desfocada. O desfoque deve ser renderizado caso todas as atualizações ocorram na área desfocada da janela, o que incorre em custos de CPU e de GPU. Além disso, as operações de janela na janela (mover/redimensionar/transições) incorrerão em mais custos.
-   Quando você espera atualizações significativas na área do cliente desfocada. Isso exigirá um redesenho do desfoque em cada atualização e consumirá recursos excessivos.
-   Se for esperado que o desfoque cubra uma área significativa e as atualizações nessa área também sejam esperadas, é altamente recomendável que você não desfoque a área do cliente.

 

 