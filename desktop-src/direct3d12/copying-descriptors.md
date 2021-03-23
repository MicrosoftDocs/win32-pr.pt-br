---
title: Copiar descritores
description: Os métodos ID3D12Device CopyDescriptors e ID3D12Device CopyDescriptorsSimple na interface do dispositivo usam a CPU para copiar descritores imediatamente.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104525"
---
# <a name="copying-descriptors"></a>Copiar descritores

Os métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) na interface do dispositivo usam a CPU para copiar imediatamente os descritores. Eles podem ser chamados de threads livres desde que vários threads na CPU ou GPU não executem gravações potencialmente conflitantes.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Copiando descritores imediatamente (linha do tempo de CPU)

O número de descritores de origem (para copiar de), especificado como um conjunto de intervalos de descrição, deve ser igual ao número de descritores de destino (para copiar), especificado como um conjunto separado de intervalos de descritores. Caso contrário, os intervalos de origem e de destino não precisam ser alinhados. Por exemplo, um conjunto esparso de descritores poderia ser copiado para um destino contíguo, vice-versa ou em alguma combinação.

Vários heaps de descritores podem ser envolvidos na operação de cópia, tanto como origem quanto destino. O uso de identificadores de descritor como parâmetros significa que os métodos de cópia não se preocupam com quais heaps um determinado descritor está. eles são apenas a memória.

Os tipos de heap de descritores sendo copiados de e para devem corresponder, portanto, os métodos usam um único tipo de heap de descritor como entrada. O driver precisa saber o tipo de heap de todos os descritores na operação de cópia fornecida, portanto, ele sabe qual é o tamanho dos dados envolvidos na operação de cópia. O driver também pode precisar fazer o trabalho de cópia personalizada se um determinado tipo de heap de descritor o garantir – um detalhe de implementação. Observe que os próprios identificadores de descritor não identificam de que tipo eles estão apontando; Portanto, um parâmetro adicional é necessário para a operação de cópia.

Uma API alternativa para [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) é fornecida para o caso simples de copiar um único intervalo de descritores de um local para outro – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).

Para esses métodos de cópia do descritor baseados em dispositivo (linha do tempo de CPU), os descritores de origem devem vir de um heap de descritor visível sem sombreador. Os descritores de destino podem estar em qualquer heap de descrição visível da CPU (sombreador visível ou não).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descritores](descriptors.md)
</dt> </dl>

 

 




