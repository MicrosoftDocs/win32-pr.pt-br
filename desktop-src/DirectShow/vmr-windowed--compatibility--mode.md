---
description: Modo de janela do VMR (compatibilidade)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Modo de janela do VMR (compatibilidade)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7312274881642d15b844e0fa950f72e52f92db8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557891"
---
# <a name="vmr-windowed-compatibility-mode"></a>Modo de janela do VMR (compatibilidade)

O VMR foi projetado para ser compatível com todos os aplicativos DirectShow existentes. Quando usado com um aplicativo existente, o VMR opera em modo de janela com um único fluxo de vídeo, também chamado de modo de compatibilidade. Esse modo é fornecido porque o VMR-7 é o renderizador padrão no Windows XP e, portanto, é usado automaticamente em chamadas para métodos de [conexão inteligente](intelligent-connect.md) , como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Se seu aplicativo usar o Intelligent Connect e exigir apenas recursos básicos de renderização, você não precisará de nenhum código especial para renderizar corretamente com o VMR-7 no Windows XP.

O VMR-9 também é executado em modo de janela/compatibilidade por padrão. No entanto, o VMR-9 nunca é o processador de vídeo padrão. Para usar o VMR-9 em um aplicativo, você deve adicioná-lo explicitamente ao gráfico de filtro. Por esse motivo, e como o modo sem janela fornece uma funcionalidade melhor do que o modo em janela, não há nenhuma vantagem específica em usar o VMR-9 no modo de janela/compatibilidade.

**Usando o VMR-7 no modo de janela/compatibilidade**

Nenhuma programação especial é necessária para configurar ou controlar o VMR-7 no modo de janela/compatibilidade. Basta criar o gráfico de filtro usando as chamadas de construção de grafo padrão, e o VMR-7 usará como padrão esse modo.

No modo em janela/compatibilidade, o VMR-7 cria sua própria janela para exibir o vídeo. Para fazer isso, ele carrega o componente do Gerenciador de janelas, que expõe as interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Seu aplicativo pode consultar o Gerenciador do grafo de filtro para essas interfaces, exatamente como você faria com o filtro de processamento de vídeo antigo. Para obter mais informações, consulte [usando o modo de janela](using-windowed-mode.md).

A ilustração a seguir mostra o VMR-7 no modo de janela/compatibilidade.

![VMR no modo de compatibilidade](images/vmr-compat-mode.png)

Para garantir o nível máximo de compatibilidade, a janela de vídeo tem o mesmo nome de classe criado pelo filtro de processamento de vídeo antigo e a maior parte do código do Gerenciador de janelas do renderizador de vídeo antigo ainda é usada pelo VMR. No modo em janela/compatibilidade, o VMR consome mais recursos do sistema do que o antigo processador de vídeo. Como o VMR-7 tem apenas um fluxo de entrada no modo de janela/compatibilidade, ele não carrega os componentes do mixer ou do compositor.

Por padrão, o VMR amplia a imagem para preencher a janela de vídeo. Para preservar a taxa de proporção da origem, chame o método [**IVMRAspectRatioControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) com o \_ sinalizador de caixa de letra ARMODE do VMR \_ \_ .

> [!Note]  
> Os aplicativos MFC que colocam a janela de vídeo em uma janela filho devem definir um \_ manipulador de mensagens ERASEBKGND do WM vazio ou a área de exibição do vídeo não será redesenhada corretamente.

 

**Usando o VMR-7 no modo de janela/compatibilidade com vários fluxos**

No modo em janela/compatibilidade, o VMR-7 cria um único PIN de entrada por padrão e desabilita o modo de combinação. Para habilitar o modo de combinação, você deve configurar o VMR antes de conectá-lo. Para obter mais informações, consulte [VMR com vários fluxos (modo de combinação)](vmr-with-multiple-streams--mixing-mode.md). No modo de combinação, o VMR carrega os componentes de mistura e com-compositor, que exigem mais recursos do sistema.

**Usando o VMR-9 em modo de janela**

Como o VMR-9 não é o renderizador padrão, ele não tem um modo de compatibilidade como esse. Em vez disso, o VMR-9 usa como padrão o modo de janela com quatro pinos de entrada. Você pode usar esse modo para misturar até quatro fluxos de vídeo. Se você precisar misturar um número maior de fluxos, deverá configurá-lo conforme descrito em [VMR com vários fluxos (modo de combinação)](vmr-with-multiple-streams--mixing-mode.md). Caso contrário, o VMR-9 em modo de janela se comporta exatamente como o VMR-7 no modo de janela/compatibilidade.

 

 



