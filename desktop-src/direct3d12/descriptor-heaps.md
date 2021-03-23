---
title: Heaps de descritores
description: Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105049"
---
# <a name="descriptor-heaps"></a>Heaps de descritores

Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral de heaps de descritores](descriptor-heaps-overview.md)<br/>                             | Heaps de descritores contêm muitos tipos de objeto que não fazem parte de um PSO (objeto de estado de pipeline), como SRVs (exibições de recursos de sombreamento), UAVs (exibições de acesso não ordenado), CBVs (exibições de buffer de constantes) e amostras. <br/>                |
| [Camadas de hardware](hardware-support.md)<br/>                                                 | Os níveis de hardware da camada 1 para a camada 3 têm recursos crescentes disponíveis para o pipeline. <br/>                                                                                                                              |
| [Heaps de descritor visíveis do sombreador](shader-visible-descriptor-heaps.md)<br/>                 | Heaps de descritores visíveis de sombreador, são heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor.<br/>                                                                                                              |
| [Heaps de descritor visíveis sem sombreador](non-shader-visible-descriptor-heaps.md)<br/>         | Alguns heaps de descritores não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparo dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível de sombreador é necessário.<br/> |
| [Criando heaps de descritor](creating-descriptor-heaps.md)<br/>                             | Para criar e configurar um heap de descritor, você deve selecionar um tipo de heap de descritor, determinar quantos descritores ele contém e definir sinalizadores que indiquem se a CPU está visível e/ou sombreador visível. <br/>                    |
| [Configurando e populando heaps de descritor](setting-descriptor-heaps.md)<br/>                | Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descrição podem ser usadas (no máximo uma de cada vez). <br/>                                                        |
| [Resumo de configurabilidade de heap do descritor](descriptor-heap-configurability-summary.md)<br/> | A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descritores](descriptors.md)
</dt> <dt>

[Tabelas de descritores](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 





