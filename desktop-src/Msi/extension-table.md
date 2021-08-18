---
description: A tabela Extensão contém informações sobre servidores de extensão de nome de arquivo que devem ser gerados como parte do anúncio do produto. Cada linha gera um conjunto de chaves e valores do Registro.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabela de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d664df812b723d7ab6c9b966b09fac8c57a35b655e123f720fdb87bdf431146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821736"
---
# <a name="extension-table"></a>Tabela de extensão

A tabela Extensão contém informações sobre servidores de extensão de nome de arquivo que devem ser gerados como parte do anúncio do produto. Cada linha gera um conjunto de chaves e valores do Registro.

A tabela Extensão contém as colunas mostradas na tabela a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Extensão   | [Text](text.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| Progid\_    | [Text](text.md)             | N   | Y        |
| Mime\_      | [Text](text.md)             | N   | Y        |
| Recurso\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extensão
</dt> <dd>

A extensão associada à linha da tabela. A extensão pode ter até 255 caracteres. Insira a extensão nesse campo sem o período anterior.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela Componente.](component-table.md) Essa coluna faz referência ao componente que controla a instalação da extensão.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>Progid\_
</dt> <dd>

A ID do Programa associada a essa extensão. Essa é uma chave estrangeira na [tabela ProgId.](progid-table.md)

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>Mime\_
</dt> <dd>

O Tipo de Conteúdo a ser gravado para a coluna Extensão.

Uma chave externa para a primeira coluna da [tabela MIME.](mime-table.md)

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Uma chave externa na primeira coluna da tabela [Recurso](feature-table.md) especificando o recurso que fornece o servidor de extensão.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela Extension é referenciada quando [a ação RegisterExtensionInfo](registerextensioninfo-action.md) ou [a ação UnRegisterExtensionInfo](unregisterextensioninfo-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



