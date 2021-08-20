---
description: A tabela IniFile contém as .ini que o aplicativo precisa definir em um .ini arquivo.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabela IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd12c02fa0123ac9e1a763b4e725681e6c6b1d51a331a1efea9916b5ac4cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946563"
---
# <a name="inifile-table"></a>Tabela IniFile

A tabela IniFile contém as .ini que o aplicativo precisa definir em um .ini arquivo.

A tabela IniFile tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identificador](identifier.md) | Y   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| DirProperty | [Identificador](identifier.md) | N   | Y        |
| Seção     | [Formatado](formatted.md)   | N   | N        |
| Chave         | [Formatado](formatted.md)   | N   | N        |
| Valor       | [Formatado](formatted.md)   | N   | N        |
| Ação      | [Inteiro](integer.md)       | N   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

A chave para esta tabela.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

O nome localizável do arquivo .ini no qual gravar as informações.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome de uma propriedade que tem um valor que é resolvido para o caminho completo da pasta que contém o .ini arquivo. A propriedade pode ser o nome de um diretório na tabela Diretório [,](directory-table.md)uma propriedade definida pela tabela [AppSearch](appsearch-table.md)ou qualquer outra propriedade que representa um caminho completo. Se esse campo for deixado em branco, .ini arquivo será criado na pasta com o caminho completo especificado pela [**propriedade WindowsFolder.**](windowsfolder.md)

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Seção
</dt> <dd>

A seção .ini arquivo.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chave
</dt> <dd>

A chave .ini arquivo localizável dentro da seção.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

O valor localizável a ser gravado.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Ação
</dt> <dd>

O tipo de modificação a ser feita.



| Constante                         | Hexadecimal | Decimal | Modification                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Cria ou atualiza uma .ini entrada.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Cria uma .ini somente se a entrada ainda não existir.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Cria uma nova entrada ou anexa um novo valor separado por vírgula a uma entrada existente. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela [Componente que](component-table.md) referencia o componente que controla a instalação do .ini valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

As .ini de arquivo são escritas quando o componente correspondente foi selecionado para ser instalado como local ou executado da origem.

Essa tabela é referenciada quando a [ação WriteIniValues](writeinivalues-action.md) ou [a ação RemoveIniValues](removeinivalues-action.md) é executada.

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

 

 



