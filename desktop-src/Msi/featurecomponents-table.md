---
description: A tabela FeatureComponents define a relação entre recursos e componentes. Para cada recurso, esta tabela lista todos os componentes que compõem esse recurso.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabela FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661563"
---
# <a name="featurecomponents-table"></a>Tabela FeatureComponents

A tabela FeatureComponents define a relação entre recursos e componentes. Para cada recurso, esta tabela lista todos os componentes que compõem esse recurso.

A tabela FeatureComponents tem as colunas a seguir.



| Coluna      | Type                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Recurso\_   | [Identificador](identifier.md) | S   | N        |
| Componente\_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Uma chave externa na primeira coluna da [tabela](feature-table.md)de recursos.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa na primeira coluna da tabela de [componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Há um limite máximo de 1600 componentes por recurso.

Os componentes podem ser compartilhados por dois ou mais recursos, ou seja, o mesmo componente pode ser referenciado por mais de um recurso.

Essa tabela é referida quando a ação [PublishFeatures](publishfeatures-action.md) ou a [ação UnpublishFeatures](unpublishfeatures-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



