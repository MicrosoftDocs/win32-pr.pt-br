---
title: Controle de risco versus recursos de pool de blocos
description: Para recursos sem blocos gráficos, o Direct3D pode impedir determinadas condições de risco durante a renderização, mas como o controle de riscos seria em um nível de bloco para recursos lado-a-quadrado, controlar condições de risco durante o processamento de recursos ao lado pode ser muito caro.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363724"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Controle de risco versus recursos de pool de blocos

Para recursos sem blocos gráficos, o Direct3D pode impedir determinadas condições de risco durante a renderização, mas como o controle de riscos seria em um nível de bloco para recursos lado-a-quadrado, controlar condições de risco durante o processamento de recursos ao lado pode ser muito caro.

Por exemplo, para os recursos que não são de lado do ladrilho, o tempo de execução não permite que nenhum determinado subrecurso seja associado como uma entrada (como um ShaderResourceView) e como uma saída (como um RenderTargetView) ao mesmo tempo. Se esse caso for encontrado, o tempo de execução desassociará a entrada. Essa sobrecarga de rastreamento no tempo de execução é barata e é feita no nível do subrecurso. Um dos benefícios dessa sobrecarga de rastreamento é minimizar as chances de aplicativos acidentalmente dependendo da ordem de execução do sombreador de hardware. A ordem de execução do sombreador de hardware pode variar se não estiver em uma determinada unidade de processamento gráfico (GPU), então certamente entre GPUs diferentes.

O rastreamento de como os recursos são associados pode ser muito caro para os recursos de blocos gráficos porque o rastreamento está em um nível de bloco. Novos problemas surgem, como possivelmente validar tentativas de processamento para um RenderTargetView com um bloco mapeado para várias áreas na superfície simultaneamente. Se acontecer desse controle de risco por bloco ser muito caro para o tempo de execução, idealmente ele seria pelo menos uma opção na camada de depuração.

Um aplicativo deve informar o driver de vídeo quando ele emitiu uma operação de gravação ou leitura para um recurso de mosaico que faz referência à memória do pool de blocos que também será referenciada por recursos separados ao lado do bloco nas operações futuras de leitura ou gravação que está esperando que a primeira operação seja concluída antes que as operações a seguir possam ser iniciadas. Para obter mais informações sobre essa condição, consulte [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) comentários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamentos estão em um pool de blocos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




