---
title: Resumo da configuração de um heap de descritores
description: A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335561"
---
# <a name="descriptor-heap-configurability-summary"></a>Resumo da configuração de um heap de descritores

A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.



|                               | Heap de descritor visível do sombreador                                                 | Heap de descritor visível não sombreador                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipos de heap com suporte**          | CBV \_ SRV \_ UAV, amostra                                                         | Tudo                                                                                                                                                                                                                                                                                                                                                                 |
| **Propriedades de página de CPU com suporte** | Não \_ disponível, combinação de gravação \_                                                 | WRITE- \_ back                                                                                                                                                                                                                                                                                                                                                         |
| **Gerenciamento de residência por aplicativo**   | Sim, aplicativo responsável                                                           | Não aplicável (não visível à GPU).                                                                                                                                                                                                                                                                                                                                   |
| **Suporte para edição de descritor**       | Somente destino de cópia, via atualização de lista de comandos e/ou cópia de CPU se a CPU estiver visível. | Somente leitura e gravação da CPU. Nenhum acesso direto à GPU. Pode ser usado para a cópia imediata da CPU (como origem e destino). Pode ser usado como uma origem de atualização em uma lista de comandos – isso copiará os descritores no armazenamento da lista de comandos durante o registro da lista de comandos. Na execução, a cópia armazenada será copiada para o destino, que deve ser um heap visível do sombreador. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




