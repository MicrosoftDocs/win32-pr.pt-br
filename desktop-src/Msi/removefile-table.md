---
description: A tabela RemoveFile contém uma lista de arquivos a serem removidos pela ação removidas. A definição da coluna FileName desta tabela como NULL dá suporte à remoção de pastas vazias.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Remover Tabelafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829187"
---
# <a name="removefile-table"></a>Remover Tabelafile

A tabela RemoveFile contém uma lista de arquivos a serem removidos pela [ação](removefiles-action.md)removidas. A definição da coluna FileName desta tabela como NULL dá suporte à remoção de pastas vazias.

A tabela RemoveFile tem as colunas a seguir.



| Coluna      | Tipo                                     | Chave | Nullable |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [Identificador](identifier.md)             | S   | N        |
| Componente\_ | [Identificador](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | S        |
| DirProperty | [Identificador](identifier.md)             | N   | N        |
| InstallMode | [Inteiro](integer.md)                   | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Chave primária usada para identificar essa entrada de tabela específica.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa a primeira coluna da [tabela de componentes](component-table.md). Este campo faz referência ao componente que controla o arquivo a ser removido.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

Esta coluna contém o nome localizável do arquivo a ser removido. Se essa coluna for nula, a pasta especificada será removida se estiver vazia. Todos os arquivos que correspondem ao curinga serão removidos do diretório especificado.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome de uma propriedade cujo valor é considerado para ser resolvido para o caminho completo da pasta do arquivo a ser removido. A propriedade pode ser o nome de um diretório na [tabela de diretórios](directory-table.md), uma propriedade definida pela [tabela AppSearch](appsearch-table.md)ou qualquer outra propriedade que represente um caminho completo.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Deve ser um dos valores a seguir.



| Constante                                | Hexadecimal | Decimal | Description                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Remover somente quando o componente associado estiver sendo instalado (msiInstallStateLocal ou msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Remover somente quando o componente associado estiver sendo removido (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Remova um dos casos acima.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

As referências de arquivo nesta tabela são processadas pela [ação RemoveFiles](removefiles-action.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 



