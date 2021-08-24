---
description: A tabela FileSFPCatalog associa os arquivos especificados aos arquivos de catálogo usados pela proteção de arquivo do sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabela FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bec6e31cba93730cc65b04ffdfb4a509f0cd817ba709cc029edfb47c4c4e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581586"
---
# <a name="filesfpcatalog-table"></a>Tabela FileSFPCatalog

A tabela FileSFPCatalog associa os arquivos especificados aos arquivos de catálogo usados pela proteção de arquivo do sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.

A tabela FileSFPCatalog tem as colunas a seguir.



| Coluna       | Tipo                         | Chave | Nullable |
|--------------|------------------------------|-----|----------|
| Arquivo\_       | [Identificador](identifier.md) | Y   | N        |
| SFPCatalog\_ | [Filename](filename.md)     | Y   | N        |



 

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

 

 



