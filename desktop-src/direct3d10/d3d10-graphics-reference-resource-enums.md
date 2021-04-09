---
description: As enumerações a seguir são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Enumerações de recursos (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010294"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a>Enumerações de recursos (gráficos do Direct3D 10)

As enumerações a seguir são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.



| Enumeração                                                     | Descrição                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**\_Sinalizador de associação de d3d10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | Identifica como um recurso será usado pelo pipeline e determina a quais estágios de pipeline um recurso pode ser associado. |
| [**\_Sinalizador de \_ acesso de CPU d3d10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | Especifica os tipos de acesso de CPU permitidos para um recurso.                                                                 |
| [**\_Dimensão DSV \_ d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | Especifica como acessar um recurso que é usado em uma exibição de estêncil de profundidade.                                                  |
| [**\_Mapa d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | Identifica um recurso a ser mapeado para leitura e gravação pela CPU.                                                    |
| [**\_Sinalizador de mapa de d3d10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | Especifica como a CPU deve responder a qualquer método de mapa quando a GPU ainda não tiver sido concluída com o recurso.               |
| [**\_Dimensão de recurso d3d10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | Identifica o tipo de recurso que está em uso.                                                                           |
| [**\_ \_ Sinalizador diverso de recurso d3d10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | Identifica opções de criação de recursos menos comuns.                                                                         |
| [**\_Dimensão d3d10 RTV \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | Especifica como acessar um recurso usado em uma exibição de destino de renderização.                                                          |
| [**Uso de D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | Identifica como um recurso deve ser lido e gravado pela CPU e/ou pela GPU.                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recurso](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



