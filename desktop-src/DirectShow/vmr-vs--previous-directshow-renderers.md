---
description: VMR versus
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: Os renderizadores do DirectShow vs. anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db40f9789a73446cb2dac4ed7033bdb163141bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768520"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>Os renderizadores do DirectShow vs. anteriores

Com os filtros antigos, os diferentes renderizadores seriam necessários no grafo, dependendo da configuração de hardware.

O filtro de [processador de vídeo](video-renderer-filter.md) foi usado para renderizar um único fluxo de vídeo em cenários de porta que não são de vídeo. Ele se baseou na tecnologia de hardware de gráficos que agora tem mais de cinco anos e em uma versão mais antiga do DirectDraw. Em determinados cenários, ele usa GDI para renderização. Isso é feito para conservar recursos de vídeo, que eram muito mais limitados há cinco anos, ou mais para superar as limitações no DirectDraw que estavam relacionadas ao suporte a vários monitores. Nem o VMR-7 nem o VMR-9 nunca usam GDI para renderização; o VMR-7 é baseado completamente no DirectDraw 7 e o VMR-9 é baseado no Direct3D 9.

Em cenários que envolvem uma porta de vídeo ou vários fluxos de entrada de vídeo, antes do VMR, o filtro de [mixer de sobreposição](overlay-mixer-filter.md) foi usado para renderização. Esse filtro usa apenas a sobreposição de hardware na placa gráfica e, portanto, é geralmente limitado a uma superfície de sobreposição fornecida pela maioria dos cartões. O mixer de sobreposição executa a criação de cores de destino, mas não é capaz de mesclagem alfa. Como ele não tem um Gerenciador de janelas, ele deve usar um segundo filtro, o processador de vídeo, para o gerenciamento de janelas. O VMR é capaz de mesclagem real alfa e pode criar várias sobreposições em software além das sobreposições de hardware.

Em cenários de porta de vídeo em que os aplicativos sobrepondo legendas codificadas ou outros dados de VBI no vídeo, um filtro adicional, o [alocador de superfície VBI](vbi-surface-allocator.md), era necessário para alocar a memória de vídeo adicional para o texto VBI. Para ISVs, o VMR-7 simplifica o desenvolvimento de aplicativos combinando a funcionalidade de alocação e renderização em um único filtro que é usado em todos os cenários. Com o VMR, o alocador de superfície VBI não é mais necessário. Esse filtro é substituído no Windows XP pelo novo filtro do [Gerenciador de portas de vídeo](video-port-manager.md) , que executa todas as tarefas de porta de vídeo executadas anteriormente pelo mixer de sobreposição.

> [!Note]  
> O VMR-9 não oferece suporte a portas de vídeo.

 

O VMR é mais robusto do que os renderizadores anteriores, em parte porque ele usa apenas o DirectDraw 7 (ou o Direct3D 9 se você estiver usando as interfaces do VMR-9), em oposição aos antigos renderizadores que usaram uma mistura de interfaces das versões mais antigas e mais recentes do DirectDraw. O VMR também emprega um novo mecanismo de apresentação de imagem projetado para gerações atuais e futuras de adaptadores, que têm suporte para Direct3D, aumento de largura de banda de memória de vídeo e VRAM e recursos de aceleração de hardware. Com o VMR, o foco está no processamento de front-end e a dependência reduzida de portas de vídeo e sobreposições. Mas, mesmo com todas as suas novas funcionalidades, o VMR foi projetado para compatibilidade máxima com os aplicativos existentes.

O VMR também é extensível. Os aplicativos podem fornecer seus próprios subcomponentes para executarem efeitos de vídeo personalizados e/ou assumir o controle da alocação e do processo de renderização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o processamento de mixagem de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



