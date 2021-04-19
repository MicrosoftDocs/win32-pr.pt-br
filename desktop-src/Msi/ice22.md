---
description: ICE22 usa a tabela FeatureComponents para validar o mapeamento de recursos e componentes referenciados na tabela PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754643"
---
# <a name="ice22"></a>ICE22

ICE22 usa a [tabela FeatureComponents](featurecomponents-table.md) para validar o mapeamento de recursos e componentes referenciados na [tabela PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Resultado

O ICE22 posta uma mensagem de erro se os recursos e componentes estiverem mapeados incorretamente na [tabela PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Exemplo

Para o exemplo a seguir, ICE22 posta um erro que não {00000003-0004-0000-0000-624474732465} tem o mapeamento correto para as \_ colunas de recurso e componente \_ .

[Tabela PublishComponent](publishcomponent-table.md) (parcial)



| ComponentId                            | Recurso\_ | Componente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[Tabela FeatureComponents](featurecomponents-table.md) (parcial)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



