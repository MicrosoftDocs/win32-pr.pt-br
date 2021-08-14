---
description: A tabela PublishComponent associa os componentes listados na tabela Component com uma cadeia de caracteres de texto qualificador e um GUID de ID de categoria.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabela PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0abd7567e8327aa36a120fd5a13115cb191e1660566e9d480446295dca53cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376379"
---
# <a name="publishcomponent-table"></a>Tabela PublishComponent

A tabela PublishComponent associa os componentes listados na tabela [Component](component-table.md) com uma cadeia de caracteres de texto qualificador e um GUID de ID de categoria. Componentes com funcionalidade paralela que foram agrupados dessa maneira são chamados de componentes qualificados. Consulte [Componentes qualificados.](qualified-components.md) Isso fornece ao instalador um método para inderção de nível único ao fazer referência a componentes. Consulte [Usando componentes qualificados.](using-qualified-components.md)

A tabela PublishComponent tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Componentid | [GUID](guid.md)             | Y   | N        |
| Qualificador   | [Text](text.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| AppData     | [Text](text.md)             | N   | Y        |
| Recurso\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

Um [GUID de cadeia](guid.md) de caracteres que representa a categoria de componentes que estão sendo agrupados. Observe que o título dessa coluna é enganoso. Esse é o GUID para a categoria de componentes qualificados e não é o mesmo GUID que aparece na coluna ComponentId da [tabela Component](component-table.md). Aqui, ele se refere a um servidor que fornece a funcionalidade de um componente para clientes externos em vez do próprio componente.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificador
</dt> <dd>

Uma cadeia de caracteres de texto que qualifica o valor na coluna ComponentId. Um qualificador é usado para distinguir várias formas do mesmo componente, como um componente implementado em vários idiomas. Essas são as cadeias de caracteres de texto do qualificador retornadas por [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na coluna um da [tabela Componente](component-table.md). Esse identificador refere-se ao registro do componente qualificado na tabela Componente.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>Appdata
</dt> <dd>

Um texto localizável opcional que descreve o componente qualificado desse registro. A cadeia de caracteres normalmente é analisado pelo aplicativo e pode ser exibida para o usuário. Ele deve descrever o componente qualificado. Isso pode ser recuperado com [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na coluna um da [tabela Recurso](feature-table.md). Esse é o recurso que usa esse componente qualificado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referenciada quando [a ação PublishComponents](publishcomponents-action.md) ou [a ação UnpublishComponents](unpublishcomponents-action.md) é executada.

Observe que o nome dessa tabela é enganoso. Essa tabela não é necessária para a adoção de anúncios. Consulte a coluna Atributos da tabela [Componente e](component-table.md) a [Tabela](feature-table.md) de recursos para obter informações sobre como definir o estado de instalação dos componentes a anunciar.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



