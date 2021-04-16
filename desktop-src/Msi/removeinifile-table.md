---
description: A tabela RemoveIniFile contém as informações que um aplicativo precisa excluir de um arquivo. ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabela RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757509"
---
# <a name="removeinifile-table"></a>Tabela RemoveIniFile

A tabela RemoveIniFile contém as informações que um aplicativo precisa excluir de um arquivo. ini.

A tabela RemoveIniFile tem as colunas a seguir.



| Coluna        | Tipo                         | Chave | Nullable |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [Identificador](identifier.md) | S   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [Identificador](identifier.md) | N   | S        |
| Seção       | [Binário](formatted.md)   | N   | N        |
| Chave           | [Binário](formatted.md)   | N   | N        |
| Valor         | [Binário](formatted.md)   | N   | S        |
| Ação        | [Inteiro](integer.md)       | N   | N        |
| Componente\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

A chave para esta tabela.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

O nome do arquivo. ini no qual as informações são excluídas.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome de uma propriedade cujo valor é considerado para ser resolvido para o caminho completo da pasta do arquivo. ini a ser removido. A propriedade pode ser o nome de um diretório na [tabela de diretórios](directory-table.md), uma propriedade definida pela [tabela AppSearch](appsearch-table.md)ou qualquer outra propriedade que represente um caminho completo.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section
</dt> <dd>

A seção do arquivo localizável. ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

A chave do arquivo localizável. ini abaixo da seção.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

O valor localizável a ser excluído. O valor é necessário quando a ação é 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

O tipo de modificação a ser feita.



| Constante                         | Hexadecimal | Decimal | Significado                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Exclui a entrada. ini.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Exclui uma marca de uma entrada. ini. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da [tabela de componentes](component-table.md) que faz referência ao componente que controla a exclusão do valor. ini.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações do arquivo. ini são excluídas quando o componente correspondente foi selecionado para ser instalado, seja localmente ou executado da origem.

Essa tabela é referida quando a [ação RemoveIniValues](removeinivalues-action.md) é executada.

Se a coluna de diretório \_ for especificada como nula, o local do arquivo ini será o local padrão do Windows ini, que é o diretório do Windows por padrão.

A remoção do último valor de uma seção exclui essa seção. Não há nenhuma outra maneira de excluir uma seção inteira que não seja remover todos os seus valores.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



