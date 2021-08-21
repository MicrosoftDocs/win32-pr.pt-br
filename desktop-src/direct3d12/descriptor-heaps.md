---
title: Heaps de descritores
description: Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd883436954cb6e1f0270646f1a57d564f3d51d29b6023bec749d1728fda40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807548"
---
# <a name="descriptor-heaps"></a>Heaps de descritores

Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral dos heaps de descritores](descriptor-heaps-overview.md)<br/>                             | Os heaps de descritor contêm muitos tipos de objeto que não fazem parte de um PSO (Objeto de Estado de Pipeline), como SRVs (Exibições de Recurso de Sombreador), UAVs (Exibições de Acesso Não Organizado), CBVs (Exibições de Buffer Constante) e Samplers. <br/>                |
| [Camadas de hardware](hardware-support.md)<br/>                                                 | Os níveis de hardware da Camada 1 para a Camada 3 têm recursos crescentes disponíveis para o pipeline. <br/>                                                                                                                              |
| [Heaps de descritores visíveis do sombreador](shader-visible-descriptor-heaps.md)<br/>                 | Heaps de descritor visíveis do sombreador são heaps de descritor que podem ser referenciados por sombreadores por meio de tabelas de descritor.<br/>                                                                                                              |
| [Heaps de descritores não visíveis do sombreador](non-shader-visible-descriptor-heaps.md)<br/>         | Alguns heaps de descritor não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparação dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível para sombreador é necessário.<br/> |
| [Como criar heaps de descritores](creating-descriptor-heaps.md)<br/>                             | Para criar e configurar um heap de descritor, você deve selecionar um tipo de heap de descritor, determinar quantos descritores ele contém e definir sinalizadores que indicam se ela está visível na CPU e/ou no sombreador visível. <br/>                    |
| [Como configurar e preencher heaps de descritores](setting-descriptor-heaps.md)<br/>                | Os tipos de heap do descritor que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descritor podem ser usadas (no máximo uma de cada uma de cada vez). <br/>                                                        |
| [Resumo da configuração de um heap de descritores](descriptor-heap-configurability-summary.md)<br/> | A tabela a seguir resume informações sobre o suporte a heap visível do sombreador e não sombreador.<br/>                                                                                                                                    |



 

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

 

 





