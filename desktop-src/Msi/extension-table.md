---
description: A tabela de extensão contém informações sobre servidores de extensão de nome de arquivo que devem ser gerados como parte do anúncio do produto. Cada linha gera um conjunto de valores e chaves do registro.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabela de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752654"
---
# <a name="extension-table"></a>Tabela de extensão

A tabela de extensão contém informações sobre servidores de extensão de nome de arquivo que devem ser gerados como parte do anúncio do produto. Cada linha gera um conjunto de valores e chaves do registro.

A tabela de extensão contém as colunas mostradas na tabela a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Extensão   | [Text](text.md)             | S   | N        |
| Componente\_ | [Identificador](identifier.md) | S   | N        |
| ProgId\_    | [Text](text.md)             | N   | S        |
| MIME\_      | [Text](text.md)             | N   | S        |
| Recurso\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extensão
</dt> <dd>

A extensão associada à linha da tabela. A extensão pode ter até 255 caracteres de comprimento. Insira a extensão neste campo sem o período anterior.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa para a primeira coluna da tabela de [componentes](component-table.md) . Esta coluna faz referência ao componente que controla a instalação da extensão.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_
</dt> <dd>

A ID do programa associada a esta extensão. Esta é uma chave estrangeira na tabela [ProgID](progid-table.md) .

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>MIME\_
</dt> <dd>

O tipo de conteúdo a ser gravado para a coluna de extensão.

Uma chave externa para a primeira coluna da tabela [MIME](mime-table.md) .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Uma chave externa na primeira coluna da tabela de [recursos](feature-table.md) que especifica o recurso que fornece o servidor de extensão.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela de extensão é referenciada quando a ação [RegisterExtensionInfo](registerextensioninfo-action.md) ou a ação [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) é executada.

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

 

 



