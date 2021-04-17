---
description: A tabela FileSFPCatalog associa os arquivos especificados aos arquivos de catálogo usados pela proteção de arquivo do sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabela FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770377"
---
# <a name="filesfpcatalog-table"></a>Tabela FileSFPCatalog

A tabela FileSFPCatalog associa os arquivos especificados aos arquivos de catálogo usados pela proteção de arquivo do sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.

A tabela FileSFPCatalog tem as colunas a seguir.



| Coluna       | Tipo                         | Chave | Nullable |
|--------------|------------------------------|-----|----------|
| Arquivo\_       | [Identificador](identifier.md) | S   | N        |
| SFPCatalog\_ | [Filename](filename.md)     | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

Chave estrangeira para a [tabela de arquivos](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

Chave estrangeira para a [tabela SFPCatalog](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A [ação InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta a [tabela de componentes](component-table.md), a [tabela de arquivos](file-table.md), a tabela FileSFPCatalog e a [tabela SFPCatalog](sfpcatalog-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



