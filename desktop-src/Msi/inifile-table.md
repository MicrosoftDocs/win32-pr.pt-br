---
description: A tabela IniFile contém as informações de. ini que o aplicativo precisa definir em um arquivo. ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabela IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010904"
---
# <a name="inifile-table"></a>Tabela IniFile

A tabela IniFile contém as informações de. ini que o aplicativo precisa definir em um arquivo. ini.

A tabela IniFile tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identificador](identifier.md) | S   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| DirProperty | [Identificador](identifier.md) | N   | S        |
| Seção     | [Binário](formatted.md)   | N   | N        |
| Chave         | [Binário](formatted.md)   | N   | N        |
| Valor       | [Binário](formatted.md)   | N   | N        |
| Ação      | [Inteiro](integer.md)       | N   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

A chave para esta tabela.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

O nome localizável do arquivo. ini no qual gravar as informações.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome de uma propriedade que tem um valor que resolve para o caminho completo da pasta que contém o arquivo. ini. A propriedade pode ser o nome de um diretório na [tabela de diretórios](directory-table.md), uma propriedade definida pela [tabela AppSearch](appsearch-table.md)ou qualquer outra propriedade que represente um caminho completo. Se esse campo for deixado em branco, o arquivo. ini será criado na pasta com o caminho completo especificado pela propriedade [**WindowsFolder**](windowsfolder.md) .

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section
</dt> <dd>

A seção do arquivo localizável. ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

A chave do arquivo localizável. ini na seção.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

O valor localizável a ser gravado.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

O tipo de modificação a ser feita.



| Constante                         | Hexadecimal | Decimal | Modification                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Cria ou atualiza uma entrada. ini.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Cria uma entrada. ini somente se a entrada ainda não existir.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Cria uma nova entrada ou acrescenta um novo valor separado por vírgula a uma entrada existente. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [componentes](component-table.md) que faz referência ao componente que controla a instalação do valor. ini.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações do arquivo. ini são gravadas quando o componente correspondente foi selecionado para ser instalado como local ou executado da origem.

Essa tabela é referida quando a ação [WriteIniValues](writeinivalues-action.md) ou a [ação RemoveIniValues](removeinivalues-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



