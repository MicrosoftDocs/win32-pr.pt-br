---
description: O ICE22 usa a tabela FeatureComponents para validar o mapeamento de recursos e componentes referenciados na tabela PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177fcef5441e5b82738c76face70427cc6865ae59c11542fca080b3dc521c5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529016"
---
# <a name="ice22"></a>ICE22

O ICE22 usa a [tabela FeatureComponents](featurecomponents-table.md) para validar o mapeamento de recursos e componentes referenciados na [tabela PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Resultado

ICE22 posta uma mensagem de erro se os recursos e componentes são mapeados incorretamente na [tabela PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Exemplo

Para o exemplo a seguir, ICE22 posta um erro que não tem o mapeamento correto para as {00000003-0004-0000-0000-624474732465} colunas Recurso \_ e \_ Componente.

[Tabela PublishComponent](publishcomponent-table.md) (parcial)



| Componentid                            | Recurso\_ | Componente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | 1º de outubro     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | 1º de outubro     | Comp2       |



 

[Tabela FeatureComponents](featurecomponents-table.md) (parcial)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| 1º de outubro     | Comp1       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



