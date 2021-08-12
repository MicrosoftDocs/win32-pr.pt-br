---
title: Considerações de desempenho e práticas recomendadas
description: Este tópico apresenta um conjunto de práticas recomendadas para usar as APIs Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), melhores práticas
- DWM (Gerenciador de Janelas da Área de Trabalho), práticas recomendadas
- Gerenciador de Janelas da Área de Trabalho (DWM), práticas de aplicativo
- DWM (Gerenciador de Janelas da Área de Trabalho), práticas de aplicativo
- Gerenciador de Janelas da Área de Trabalho (DWM), práticas de desenho
- DWM (Gerenciador de Janelas da Área de Trabalho), práticas de desenho
- Gerenciador de Janelas da Área de Trabalho (DWM), desfoque por trás do efeito
- DWM (Gerenciador de Janelas da Área de Trabalho), desfoque por trás do efeito
- práticas de aplicativo
- práticas de desenho
- efeito de desfoque por trás
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7affbbf5ebca91a4e5172e75f88da4b9fe8e33f6e1e3de1e7a735add816a313f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280269"
---
# <a name="performance-considerations-and-best-practices"></a>Considerações de desempenho e práticas recomendadas

Este tópico apresenta um conjunto de práticas recomendadas para usar as APIs Gerenciador de Janelas da Área de Trabalho (DWM).

Este tópico contém as seguintes seções:

-   [Práticas de aplicativo para DWM](#application-practices-for-dwm)
-   [Práticas de desenho para DWM](#drawing-practices-for-dwm)
-   [Região do cliente Blur-Behind DWM](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Práticas de aplicativo para DWM

Se seu aplicativo manipular o dimensionamento dpi (pontos por polegada), você poderá declarar um aplicativo como com conhecimento de dpi e impedir o dimensionamento automático definindo o sinalizador com conhecimento de dpi no manifesto do programa ou chamando a função [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) durante a inicialização do programa.

Com a composição DWM posicionada, os aplicativos obscurecidos não recebem mais mensagens [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) e não são solicitados a renderizar. O conteúdo de cada janela já está disponível para compor a imagem da tela.

As janelas [**TRANSPARENTES do WS \_ EX \_ de**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) nível superior devem ser combinadas com um estilo **WS \_ EX \_ LAYERED** para fins de teste de acerto. **WS \_ EX \_ TRANSPARENT** no sentido clássico, sem redirecionamento, é útil para janelas filho em uma hierarquia de janelas que pertencem ao mesmo thread, mas não se destina a janelas de nível superior.

Use regiões ou camadas para criar janelas formaadas ou mescladas. Observe que, no Windows Vista e versões posteriores do Windows, o desenho personalizado apenas parte de uma janela de nível superior não fornecerá o conteúdo desleixado desejado em regiões não redesenhadas.

APIs como [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) podem ser usadas para determinar determinados valores reais. Se você tiver um DC (contexto de dispositivo) para uma janela redirecionada, a origem retornada por **GetDCOrgEx** não corresponderá à origem da janela na tela. Em vez disso, a origem será a origem da superfície do buffer de fundo para sua janela: (0, 0).

Quando todo o resto falhar, desabilite a renderização de janela chamando [**a função DwmSetWindowAttribute.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)

## <a name="drawing-practices-for-dwm"></a>Práticas de desenho para DWM

Evite desenhar diretamente para a superfície de exibição primária. Isso força o DWM a desabilitar a composição até que seu aplicativo libere a superfície do dispositivo primário.

Avalie se seu aplicativo deve fornecer seu próprio buffer duplo. O DWM efetivamente duplica o conteúdo e apresenta a janela em um único quadro.

Evite ler ou escrever em um DC de exibição. Embora o DWM tenha suporte, não recomendamos isso devido à diminuição do desempenho.

Evite desenhar na área não cliente. Embora essa área possa ser acessada pelo aplicativo e o desenho seja suportado pela API do Microsoft Win32, isso pode fazer com que a janela perca qualquer borda de vidro que ela tenha.

Evite misturar Windows Graphics Device Interface (GDI) e Microsoft DirectX, a menos que eles não se sobreponham. Se a combinação for necessária, desenhe o conteúdo GDI em uma superfície de software DirectX e combine-os antes de compor na tela ou desenhá-los em janelas separadas.

Use [**a função BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) [**ou StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) em vez de Windows GDI+ para apresentar seu desenho para renderização. GDI+ renderiza uma linha de verificação por vez com a renderização de software. Isso pode causar cintilação em seus aplicativos.

## <a name="dwm-blur-behind-client-region"></a>Região do cliente Blur-Behind DWM

Renderizar o efeito de desfoque é uma operação com uso intensivo de recursos para a CPU e a GPU (unidade de processamento gráfico). Os desenvolvedores de aplicativos são incentivados a considerar as implicações do uso do desfoque da área do cliente para que ele não consuma recursos excessivos. Você deve ter cuidado específico nos seguintes casos:

-   Quando você espera que o tamanho do desfoque da área do cliente seja significativo, mesmo que nenhuma atualização ocorra na própria área desfoque. O desfoque deve ser renderizado no caso de qualquer atualização ocorrer na área desfoque da janela, o que incorre em custos de CPU e GPU. Além disso, as operações de janela na janela (mover/resize/transições) incorrerão em mais custos.
-   Quando você espera atualizações significativas na área de cliente desfocado. Isso exigirá uma nova reintição do desfoque em cada atualização e consumirá recursos excessivos.
-   Se o desfoque for esperado para abranger uma área significativa e as atualizações para essa área também são esperadas, é altamente recomendável que você não desfoque a área do cliente.

 

 