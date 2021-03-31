---
description: A tabela Replicafile contém uma lista de arquivos que devem ser duplicados, seja para um diretório diferente do arquivo original ou para o mesmo diretório, mas com um nome diferente. O arquivo original deve ser um arquivo instalado pela ação InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Tabela replicafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011153"
---
# <a name="duplicatefile-table"></a>Tabela replicafile

A tabela Replicafile contém uma lista de arquivos que devem ser duplicados, seja para um diretório diferente do arquivo original ou para o mesmo diretório, mas com um nome diferente. O arquivo original deve ser um arquivo instalado pela [ação InstallFiles](installfiles-action.md).

A tabela Replicafile tem as colunas a seguir.



| Coluna      | Type                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| FileKey     | [Identificador](identifier.md) | S   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Arquivo\_      | [Identificador](identifier.md) | N   | N        |
| Destname    | [Filename](filename.md)     | N   | S        |
| DestFolder  | [Identificador](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Uma chave primária, um token não localizado, identificando um registro de Duplicatafiles exclusivo.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela de componentes](component-table.md). Se o componente identificado pela chave não estiver selecionado para instalação ou remoção, nenhuma ação será executada nesse registro duplicado.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

Chave estrangeira na [tabela de arquivos](file-table.md) que representa o arquivo original a ser duplicado.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname
</dt> <dd>

Nome localizável a ser dado ao arquivo duplicado. Se esse campo estiver em branco, o arquivo de destino receberá o mesmo nome do arquivo original.

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Nome de uma propriedade que é o caminho completo para onde o arquivo duplicado deve ser copiado. Se esse diretório for o mesmo que o diretório que contém o arquivo original e o nome do arquivo duplicado proposto for o mesmo que o original, nenhuma ação ocorrerá.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela é processada pela [ação DuplicateFiles](duplicatefiles-action.md) e a [ação RemoveDuplicateFiles](removeduplicatefiles-action.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
</dl>

 

 



