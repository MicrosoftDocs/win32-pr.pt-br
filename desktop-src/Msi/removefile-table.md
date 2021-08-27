---
description: A tabela RemoveFile contém uma lista de arquivos a serem removidos pela ação RemoveFiles. Definir a coluna FileName desta tabela como Null dá suporte à remoção de pastas vazias.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Tabela RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cf63e9b7616eb033a696da2ad29cb4310e6dc0dc56279ef465c3c549cb5437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082596"
---
# <a name="removefile-table"></a>Tabela RemoveFile

A tabela RemoveFile contém uma lista de arquivos a serem removidos pela [ação RemoveFiles](removefiles-action.md). Definir a coluna FileName desta tabela como Null dá suporte à remoção de pastas vazias.

A tabela RemoveFile tem as seguintes colunas.



| Coluna      | Tipo                                     | Chave | Nullable |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [Identificador](identifier.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | Y        |
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

Chave externa da primeira coluna da [tabela Componente](component-table.md). Esse campo faz referência ao componente que controla o arquivo a ser removido.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Essa coluna contém o nome localizável do arquivo a ser removido. Se essa coluna for nula, a pasta especificada será removida se estiver vazia. Todos os arquivos que corresponderem ao curinga serão removidos do diretório especificado.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome de uma propriedade cujo valor deve ser resolvido para o caminho completo para a pasta do arquivo a ser removido. A propriedade pode ser o nome de um diretório na tabela Diretório [,](directory-table.md)uma propriedade definida pela tabela [AppSearch](appsearch-table.md)ou qualquer outra propriedade que representa um caminho completo.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Deve ser um dos valores a seguir.



| Constante                                | Hexadecimal | Decimal | Descrição                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Remova somente quando o componente associado estiver sendo instalado (msiInstallStateLocal ou msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Remova somente quando o componente associado estiver sendo removido (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Remova em qualquer um dos casos acima.                                                                          |



 

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

 

 



