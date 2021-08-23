---
description: A tabela FeatureComponents define a relação entre recursos e componentes. Para cada recurso, esta tabela lista todos os componentes que comem esse recurso.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabela FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7635a43784ee7e8fbb71c7161bb07d39ffe5238177ea2a7cdaabdeb18dc41e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430866"
---
# <a name="featurecomponents-table"></a>Tabela FeatureComponents

A tabela FeatureComponents define a relação entre recursos e componentes. Para cada recurso, esta tabela lista todos os componentes que comem esse recurso.

A tabela FeatureComponents tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Recurso\_   | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Uma chave externa na primeira coluna da tabela [Recurso](feature-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa na primeira coluna da [tabela Componente](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Há um limite máximo de 1600 componentes por recurso.

Os componentes podem ser compartilhados por dois ou mais recursos, ou seja, o mesmo componente pode ser referenciado por mais de um recurso.

Essa tabela é referenciada quando [a ação PublishFeatures](publishfeatures-action.md) ou [a ação UnpublishFeatures](unpublishfeatures-action.md) é executada.

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

 

 



