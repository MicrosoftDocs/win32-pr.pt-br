---
title: Resumo de configurabilidade de heap do descritor
description: A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105047"
---
# <a name="descriptor-heap-configurability-summary"></a>Resumo de configurabilidade de heap do descritor

A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.



|                               | Heap de descritor visível do sombreador                                                 | Heap de descritor visível não sombreador                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipos de heap com suporte          | CBV \_ SRV \_ UAV, amostra                                                         | Tudo                                                                                                                                                                                                                                                                                                                                                                 |
| Propriedades de página de CPU com suporte | Não \_ disponível, combinação de gravação \_                                                 | WRITE- \_ back                                                                                                                                                                                                                                                                                                                                                         |
| Gerenciamento de residência por aplicativo   | Sim, aplicativo responsável                                                           | Não aplicável (não visível à GPU).                                                                                                                                                                                                                                                                                                                                   |
| Suporte para edição de descritor       | Somente destino de cópia, via atualização de lista de comandos e/ou cópia de CPU se a CPU estiver visível. | Somente leitura e gravação da CPU. Nenhum acesso direto à GPU. Pode ser usado para a cópia imediata da CPU (como origem e destino). Pode ser usado como uma origem de atualização em uma lista de comandos – isso copiará os descritores no armazenamento da lista de comandos durante o registro da lista de comandos. Na execução, a cópia armazenada será copiada para o destino, que deve ser um heap visível do sombreador. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




