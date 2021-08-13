---
title: Redimensionamento de pool de blocos
description: Use a API ID3D11DeviceContext2 ResizeTilePool para aumentar um pool de blocos se o aplicativo precisar de mais um conjunto de trabalho para o mapeamento de recursos lado-a-quadro ou para reduzir se for necessário menos espaço.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b91e3942e5da88c58c391f652a2b23a7b02513777060d78e86522b892da478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375806"
---
# <a name="tile-pool-resizing"></a>Redimensionamento de pool de blocos

Use a API [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) para aumentar um pool de blocos se o aplicativo precisar de mais um conjunto de trabalho para o mapeamento de recursos lado-a-quadro ou para reduzir se for necessário menos espaço. Outra opção para aplicativos é alocar pools de blocos adicionais para novos recursos ao lado. Mas, se qualquer recurso de lado único precisar de mais espaço do que inicialmente disponível em seu pool de peças, o aumento do pool de blocos é uma boa opção. Um recurso por lado não pode ter mapeamentos em vários pools de blocos ao mesmo tempo.

Quando um pool de blocos é expandido, blocos adicionais são adicionados ao final por meio de uma ou mais alocações novo pelo driver de vídeo. Essa divisão em alocações não fica visível para o aplicativo. A memória existente no pool de blocos é deixada inalterada, e os mapeamentos de recursos de mosaico existentes nessa memória permanecem intactos.

Quando um pool de blocos é reduzido, os blocos são removidos do final. Os blocos são removidos até mesmo abaixo do tamanho de alocação inicial, até 0, o que significa que novos mapeamentos não poderão ser feitos após o novo tamanho. Porém, os mapeamentos existentes após o final do novo tamanho permanecem intactos e utilizáveis. O driver de vídeo manterá a memória ativa enquanto permanecerem mapeamentos para qualquer parte das alocações que o driver usa para a memória do pool de blocos. Se, após a redução, parte da memória for mantida ativa porque mapeamentos de blocos são apontando para ela e, em seguida, o pool de blocos for ampliado novamente (em qualquer valor), a memória existente será reutilizada primeiro antes que qualquer alocação adicional ocorra para atender ao tamanho da operação de ampliação.

Para poder economizar memória, o aplicativo precisa não só reduzir um pool de blocos, mas também remover/remapear os mapeamentos existentes após o final do novo tamanho de pool de blocos menor.

O ato de reduzir (e remover mapeamentos) não necessariamente gera economia de memória de imediato. A liberação da memória depende de quão granulares as alocações subjacentes do driver de vídeo são para o pool de blocos. Quando a redução é suficiente para fazer uma alocação de driver de vídeo não utilizado, o driver de vídeo pode liberá-la. Se um pool de blocos foi ampliado, a redução aos tamanhos anteriores (e remover/remapear os mapeamentos de blocos de forma correspondente) tem grandes chances de economizar memória, embora não haja garantia caso os tamanhos não se alinhem exatamente aos tamanhos de alocação subjacentes escolhidos pelo driver de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamentos estão em um pool de blocos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




