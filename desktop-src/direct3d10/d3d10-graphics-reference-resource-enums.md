---
description: As enumerações a seguir são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Enumerações de recursos (elementos gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc82ac605c8ab4dd6ead6ea392dc30db67cd777642dbaab0b9f57520353a467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989555"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a>Enumerações de recursos (elementos gráficos do Direct3D 10)

As enumerações a seguir são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.



| Enumeração                                                     | Descrição                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**SINALIZADOR BIND D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | Identifica como um recurso será usado pelo pipeline e determina a quais estágios de pipeline um recurso pode ser vinculado. |
| [**SINALIZADOR DE ACESSO À CPU D3D10 \_ \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | Especifica os tipos de acesso à CPU permitidos para um recurso.                                                                 |
| [**DIMENSÃO D3D10 \_ DSV \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | Especifica como acessar um recurso usado em uma exibição de estêncil de profundidade.                                                  |
| [**D3D10 \_ MAP**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | Identifica um recurso a ser mapeado para leitura e escrita pela CPU.                                                    |
| [**SINALIZADOR DE MAPA D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | Especifica como a CPU deve responder a qualquer método map quando a GPU ainda não foi concluída com o recurso.               |
| [**DIMENSÃO DE RECURSOS D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | Identifica o tipo de recurso que está em uso.                                                                           |
| [**SINALIZADOR MISC DO RECURSO D3D10 \_ \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | Identifica opções de criação de recursos menos comuns.                                                                         |
| [**DIMENSÃO D3D10 \_ RTV \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | Especifica como acessar um recurso usado em uma exibição de destino de renderização.                                                          |
| [**USO DE D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | Identifica como um recurso deve ser lido e gravado pela CPU e/ou pela GPU.                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



