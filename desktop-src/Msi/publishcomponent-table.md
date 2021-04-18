---
description: A tabela PublishComponent associa os componentes listados na tabela de componentes com uma cadeia de caracteres de texto de qualificador e um GUID de ID de categoria.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabela PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759644"
---
# <a name="publishcomponent-table"></a>Tabela PublishComponent

A tabela PublishComponent associa os componentes listados na [tabela de componentes](component-table.md) com uma cadeia de caracteres de texto de qualificador e um GUID de ID de categoria. Os componentes com funcionalidade paralela que foram agrupados dessa maneira são chamados de componentes qualificados. Consulte [componentes qualificados](qualified-components.md). Isso fornece ao instalador um método de indireção de nível único ao fazer referência aos componentes. Consulte [usando componentes qualificados](using-qualified-components.md).

A tabela PublishComponent tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| ComponentId | [GUID](guid.md)             | S   | N        |
| Qualificador   | [Text](text.md)             | S   | N        |
| Componente\_ | [Identificador](identifier.md) | S   | N        |
| AppData     | [Text](text.md)             | N   | S        |
| Recurso\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

Um [GUID](guid.md) de cadeia de caracteres que representa a categoria de componentes agrupados. Observe que o título desta coluna é enganoso. Este é o GUID para a categoria de componentes qualificados e não é o mesmo GUID que aparece na coluna ComponentID da [tabela de componentes](component-table.md). Aqui, ele se refere a um servidor que fornece a funcionalidade de um componente para clientes externos em vez do próprio componente.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificado
</dt> <dd>

Uma cadeia de texto que qualifica o valor na coluna ComponentID. Um qualificador é usado para distinguir várias formas do mesmo componente, como um componente que é implementado em vários idiomas. Essas são as cadeias de texto do qualificador retornadas por [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na coluna um da [tabela de componentes](component-table.md). Esse identificador se refere ao registro do componente qualificado na tabela de componentes.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData
</dt> <dd>

Um texto localizável opcional que descreve o componente qualificado deste registro. A cadeia de caracteres é normalmente analisada pelo aplicativo e pode ser exibida para o usuário. Ele deve descrever o componente qualificado. Isso pode ser recuperado com [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na coluna um da [tabela de recursos](feature-table.md). Esse é o recurso que usa esse componente qualificado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a ação [PublishComponents](publishcomponents-action.md) ou a [ação UnpublishComponents](unpublishcomponents-action.md) é executada.

Observe que o nome desta tabela é enganoso. Essa tabela não é necessária para criar anúncios. Consulte a coluna atributos da tabela de [componentes](component-table.md) e a [tabela de recursos](feature-table.md) para obter informações sobre como definir o estado de instalação dos componentes a serem anunciados.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



