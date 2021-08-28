---
description: Modo de janela de VMR (compatibilidade)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Modo de janela de VMR (compatibilidade)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d27a5a115ac87475a27365a0211d93cf18e785983cda12ee338e73b24fb0f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049286"
---
# <a name="vmr-windowed-compatibility-mode"></a>Modo de janela de VMR (compatibilidade)

A VMR foi projetada para ser compatível com todos os aplicativos DirectShow existentes. Quando ele é usado com um aplicativo existente, a VMR opera no modo em janelas com um único fluxo de vídeo, também chamado de modo de compatibilidade. Esse modo é fornecido porque a VMR-7 é o renderador padrão no Windows XP e, portanto, é usado automaticamente em chamadas para métodos inteligentes [do Conexão,](intelligent-connect.md) como [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Se seu aplicativo usar o Intelligent Conexão e exigir apenas recursos básicos de renderização, você não precisará de nenhum código especial para renderizar corretamente com a VMR-7 no Windows XP.

A VMR-9 também é executado no modo de janela/compatibilidade por padrão. No entanto, a VMR-9 nunca é o renderador de vídeo padrão. Para usar a VMR-9 em um aplicativo, você deve adicioná-la explicitamente ao grafo de filtro. Por esse motivo, e como o modo sem janelas fornece uma funcionalidade melhor do que o modo em janelas, não há nenhuma vantagem específica de usar a VMR-9 no modo de janela/compatibilidade.

**Usando a VMR-7 no modo de janela/compatibilidade**

Nenhuma programação especial é necessária para configurar ou controlar a VMR-7 no modo de janela/compatibilidade. Basta criar o grafo de filtro usando as chamadas padrão de criação de grafo e a VMR-7 será padrão para esse modo.

No modo de janela/compatibilidade, a VMR-7 cria sua própria janela para exibir o vídeo. Para fazer isso, ele carrega o componente gerenciador de janelas, que expõe as interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Seu aplicativo pode consultar o Gerenciador Graph filtro para essas interfaces, exatamente como você faria com o filtro antigo do Video Renderer. Para obter mais informações, consulte [Usando o modo em janelas.](using-windowed-mode.md)

A ilustração a seguir mostra a VMR-7 no modo de janela/compatibilidade.

![vmr no modo de compatibilidade](images/vmr-compat-mode.png)

Para garantir o nível máximo de compatibilidade, a janela de vídeo tem o mesmo nome de classe que aquele criado pelo filtro antigo do Renderador de Vídeo e a maioria do código do Gerenciador de Janelas do Renderador de Vídeo antigo ainda é usada pela VMR. No modo de janela/compatibilidade, a VMR não consome mais recursos do sistema do que o Renderador de Vídeo antigo. Como a VMR-7 tem apenas um fluxo de entrada no modo de janela/compatibilidade, ela não carrega seus componentes de mixer ou compositor.

Por padrão, a VMR alonga a imagem para preencher a janela de vídeo. Para preservar a taxa de proporção da origem, chame o [**método IVMRAspectRatioControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) com o sinalizador \_ ARMODE LETTER BOX da VMR. \_ \_

> [!Note]  
> Os aplicativos MFC que agem na janela de vídeo em uma janela filho devem definir um manipulador de mensagens WM ERASEBKGND vazio ou a área de exibição de vídeo não será \_ reintint corretamente.

 

**Usando a VMR-7 no modo de janela/compatibilidade com várias Fluxos**

No modo de janela/compatibilidade, a VMR-7 cria um único pino de entrada por padrão e desabilita o modo de combinação. Para habilitar o modo de combinação, você deve configurar a VMR antes de conectá-la. Para obter mais informações, [consulte VMR com vários Fluxos (modo de combinação).](vmr-with-multiple-streams--mixing-mode.md) No modo de combinação, a VMR carrega os componentes de combinação e compositor, que exigem mais recursos do sistema.

**Usando a VMR-9 no modo em janelas**

Como a VMR-9 não é o renderador padrão, ela não tem um modo de compatibilidade como tal. Em vez disso, a VMR-9 assume como padrão o modo de janela com quatro pinos de entrada. Você pode usar esse modo para misturar até quatro fluxos de vídeo. Se você precisar misturar um número maior de fluxos, deverá configurá-lo conforme descrito em VMR com vários [Fluxos (modo de combinação).](vmr-with-multiple-streams--mixing-mode.md) Caso contrário, a VMR-9 no modo de janela se comportará exatamente como a VMR-7 no modo de janela/compatibilidade.

 

 



