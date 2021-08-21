---
description: Esta tabela contém uma lista de arquivos a serem movidos ou copiados de um diretório de origem especificado para um diretório de destino especificado.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabela MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d90afe8a5fb950f2e6fdb96ba0f8af4f8969226a5dc219bc9cd0598481beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945091"
---
# <a name="movefile-table"></a>Tabela MoveFile

Esta tabela contém uma lista de arquivos a serem movidos ou copiados de um diretório de origem especificado para um diretório de destino especificado.

A tabela MoveFile tem as colunas a seguir.



| Coluna       | Tipo                         | Chave | Nullable |
|--------------|------------------------------|-----|----------|
| FileKey      | [Identificador](identifier.md) | Y   | N        |
| Componente\_  | [Identificador](identifier.md) | N   | N        |
| SourceName   | [Text](text.md)             | N   | Y        |
| Destname     | [Filename](filename.md)     | N   | Y        |
| SourceFolder | [Identificador](identifier.md) | N   | Y        |
| DestFolder   | [Identificador](identifier.md) | N   | N        |
| Opções      | [Inteiro](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Chave primária que identifica exclusivamente um registro MoveFile específico.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na [tabela de componentes](component-table.md). Se o componente referenciado por essa chave não estiver selecionado para instalação ou remoção, nenhuma ação será executada nessa entrada MoveFile.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

Esta coluna contém o nome localizável dos arquivos de origem a serem movidos ou copiados. Esta coluna pode ser deixada em branco. Consulte a descrição da coluna SourceFolder. Este campo deve conter um nome de arquivo longo e pode conter caracteres curinga ( \* e?).

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname
</dt> <dd>

Esta coluna contém o nome localizável a ser dado ao arquivo original após ser movido ou copiado. Se esse campo estiver em branco, o arquivo de destino receberá o mesmo nome que o arquivo de origem.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder
</dt> <dd>

Esta coluna contém o nome de uma propriedade que tem um valor que resolve para o caminho completo para o diretório de origem. Se a coluna SourceName for deixada em branco, a propriedade chamada na coluna SourceFolder será considerada para conter o caminho completo para o próprio arquivo de origem (incluindo o nome do arquivo).

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

O nome de uma propriedade cujo valor é resolvido para o caminho completo do diretório de destino.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opções
</dt> <dd>

Valor inteiro que especifica o modo de operação.



| Constante                     | Hexadecimal | Decimal | Significado               |
|------------------------------|-------------|---------|-----------------------|
| (nenhum)                       | 0x000       | 0       | Copie o arquivo de origem. |
| **msidbMoveFileOptionsMove** | 0x001       | 1       | Mova o arquivo de origem. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se um \* caractere curinga "" for inserido na coluna SourceName da tabela MoveFile e um nome de arquivo de destino for especificado na coluna destname, todos os arquivos movidos ou copiados manterão os nomes nas fontes.

Essa tabela é processada pela [ação MoveFiles](movefiles-action.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 



