---
title: Subalocação dentro de heaps
description: Heaps de recursos transferem dados da CPU para a GPU (carregamento) e da GPU para a CPU (leitura de volta).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104873"
---
# <a name="suballocation-within-heaps"></a>Subalocação dentro de heaps

Heaps de recursos transferem dados da CPU para a GPU (carregamento) e da GPU para a CPU (leitura de volta).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alias de memória e herança de dados](memory-aliasing-and-data-inheritance.md)<br/> | O recurso colocado e reservado pode alias de memória física em um heap. Os recursos inseridos permitem mais cenários de herança de dados do que os recursos reservados quando o heap tem o sinalizador compartilhado definido ou quando os recursos com alias têm layouts de memória totalmente definidos. <br/> |
| [Heaps compartilhados](shared-heaps.md)<br/>                                                 | O compartilhamento é útil para arquiteturas de vários processos e multiadaptadores.<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID3D12Device:: createheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gerenciamento de memória](memory-management.md)
</dt> </dl>

 

 





