---
title: Contadores de saída de fluxo
description: A saída de fluxo é a capacidade da GPU de gravar vértices em um buffer. Os contadores de saída do fluxo monitoram o progresso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103773"
---
# <a name="stream-output-counters"></a>Contadores de saída de fluxo

A saída de fluxo é a capacidade da GPU de gravar vértices em um buffer. Os contadores de saída do fluxo monitoram o progresso.

-   [Diferenças nos contadores de fluxo do Direct3D 11 para o Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Tópicos relacionados](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Diferenças nos contadores de fluxo do Direct3D 11 para o Direct3D 12

Como parte do processo de saída de fluxo, a GPU precisa saber o local atual no buffer em que está gravando. No Direct3D 11, a memória para armazenar esse local é alocada pelo driver e a única maneira de os aplicativos manipular esse valor é por meio do método **SOSetTargets** . No Direct3D 12, os aplicativos alocam memória para armazenar esse local atual. Não há maneiras especiais de manipular esse valor, e os aplicativos são livres para ler/gravar o valor com a CPU ou a GPU.

## <a name="bufferfilledsize"></a>BufferFilledSize

O aplicativo é responsável por alocar armazenamento para uma quantidade de 32 bits chamada *BufferFilledSize*. Contém o número de bytes de dados no buffer de saída de fluxo. Esse armazenamento pode ser colocado no mesmo recurso, ou em outro, como aquele que contém os dados de saída de fluxo. Esse valor é acessado pela GPU no estágio Stream-Output para determinar onde acrescentar novos dados de vértice no buffer. Além disso, esse valor é acessado pela GPU para determinar quando o estouro ocorreu.

Consulte o D3D12 de [**saída de fluxo de estrutura \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

A camada de depuração validará o seguinte em [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *BufferFilledSize* cai no intervalo implícito por {*OffsetInBytes*, *sizeInBytes*}, se um recurso não nulo for especificado.
-   *BufferFilledSizeOffsetInBytes* é um múltiplo de 4.
-   *BufferFilledSizeOffsetInBytes* está dentro do intervalo do recurso que o contém.
-   O recurso especificado é um buffer.

O tempo de execução não validará o tipo de heap associado ao buffer de saída de fluxo, pois a saída de fluxo terá suporte em todos os tipos de heap.

As assinaturas raiz devem especificar se a saída do fluxo será usada usando os sinalizadores de [**\_ \_ \_ sinalizadores de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .

\_ \_ O sinalizador de assinatura raiz D3D12 \_ \_ permitirá que \_ \_ a saída de fluxo possa ser especificada para assinaturas raiz criadas em HLSL, de maneira semelhante a como os outros sinalizadores são especificados.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) falhará se o sombreador de geometria contiver Stream-output, mas a assinatura raiz não tiver o sinalizador de \_ assinatura raiz D3D12 \_ \_ \_ permitir \_ conjunto de sinalizadores de saída de fluxo \_ .

Quando um recurso é usado como um destino de saída de fluxo, os recursos usados devem estar no \_ estado do fluxo de estado do recurso D3D12 \_ \_ \_ . Isso se aplica aos dados de vértice e ao *BufferFilledSize* (que pode estar nos mesmos ou em recursos separados).

Não há nenhuma API especial para definir deslocamentos de buffer de saída de fluxo porque os aplicativos podem gravar no *BufferFilledSize* com a CPU ou GPU diretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contadores e consultas](counters-and-queries.md)
</dt> </dl>

 

 




