---
description: A tabela de verbos contém informações de verbo de comando associadas a extensões de nome de arquivo que devem ser geradas como parte do anúncio do produto. Cada linha gera um conjunto de valores e chaves do registro.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabela de verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fc546cd3db5fecb3861120fa15b1ffa3f21327b889599b77a1b067193c886c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499106"
---
# <a name="verb-table"></a>Tabela de verbo

A tabela de verbos contém informações de verbo de comando associadas a extensões de nome de arquivo que devem ser geradas como parte do anúncio do produto. Cada linha gera um conjunto de valores e chaves do registro.

A tabela de verbos tem as colunas a seguir.



| Coluna      | Tipo                       | Chave | Nullable |
|-------------|----------------------------|-----|----------|
| Extensão\_ | [Text](text.md)           | Y   | N        |
| Verbo        | [Text](text.md)           | Y   | N        |
| Sequência    | [Inteiro](integer.md)     | N   | Y        |
| Comando     | [Binário](formatted.md) | N   | Y        |
| Argumento    | [Binário](formatted.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensão\_
</dt> <dd>

A extensão associada à linha da tabela. Esta coluna é uma chave externa para a primeira coluna da [tabela de extensão](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo
</dt> <dd>

O verbo para o comando.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

A sequência dos comandos. Somente os verbos para os quais a coluna de sequência é não nula são usados para preparar uma lista ordenada para o valor padrão da chave do Shell. O verbo com o menor valor nessa coluna torna-se o verbo padrão.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Linha
</dt> <dd>

O texto localizável exibido no menu de contexto.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Valor para os argumentos do comando.

Observe que a resolução das propriedades no campo argumento é limitada. Uma propriedade formatada como \[ *Propriedade* \] nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente proprietário do verbo for instalado. Por exemplo, para o argumento " \[ \#MyDoc.doc\] " para resolver o valor correto, o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui o verbo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a ação [RegisterExtensionInfo](registerextensioninfo-action.md) ou a [ação UnregisterExtensionInfo](unregisterextensioninfo-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



