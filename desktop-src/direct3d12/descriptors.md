---
title: Descritores
description: Os descritores são a unidade primária de associação para um único recurso no D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104289"
---
# <a name="descriptors"></a>Descritores

Os descritores são a unidade primária de associação para um único recurso no D3D12.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral dos descritores](descriptors-overview.md)<br/> | Os descritores são criados por chamadas à API e identificam recursos.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Criando descritores](creating-descriptors.md)<br/> | Descreve e mostra exemplos de como criar exibições de índice, vértice e buffer constante; recurso de sombreador, destino de renderização, acesso não ordenado, saída de fluxo e exibições de estêncil de profundidade; e amostras. Todos os métodos para criar descritores são threads livres.<br/>                                                                                                                             |
| [Copiar descritores](copying-descriptors.md)<br/>   | Os métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) na interface do dispositivo usam a CPU para copiar imediatamente os descritores. Eles podem ser chamados de threads livres desde que vários threads na CPU ou GPU não executem gravações potencialmente conflitantes.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> <dt>

[Tabelas de descritores](descriptor-tables.md)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 





