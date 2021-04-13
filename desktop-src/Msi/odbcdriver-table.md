---
description: A tabela ODBCDriver lista os drivers ODBC que pertencem à instalação.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabela ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501565"
---
# <a name="odbcdriver-table"></a>Tabela ODBCDriver

A tabela ODBCDriver lista os drivers ODBC que pertencem à instalação.

A tabela ODBCDriver tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Driver      | [Identificador](identifier.md) | S   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Descrição | [Text](text.md)             | N   | N        |
| Arquivo\_      | [Identificador](identifier.md) | N   | N        |
| Configuração de arquivo \_ | [Identificador](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver
</dt> <dd>

Nome do token interno para o driver. Uma chave primária para a tabela

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na tabela de componentes.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

A descrição registrada para este driver ODBC. Este valor não pode ser localizado.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

O arquivo DLL para os drivers listados na coluna driver. A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md). O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto. A \| sintaxe SFN LFN não pode ser usada.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuração de arquivo \_
</dt> <dd>

O arquivo DLL de instalação para o driver se ele for diferente do driver. A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md). O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto. A \| sintaxe SFN LFN não pode ser usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



