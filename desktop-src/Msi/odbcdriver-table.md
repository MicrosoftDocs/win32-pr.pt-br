---
description: A tabela ODBCDriver lista os drivers ODBC que pertencem à instalação.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabela ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943117"
---
# <a name="odbcdriver-table"></a>Tabela ODBCDriver

A tabela ODBCDriver lista os drivers ODBC que pertencem à instalação.

A tabela ODBCDriver tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Driver      | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Descrição | [Text](text.md)             | N   | N        |
| Arquivo\_      | [Identificador](identifier.md) | N   | N        |
| Configuração de \_ arquivo | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver
</dt> <dd>

Nome do token interno para o driver. Uma chave primária para a tabela

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na tabela Componente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

A descrição registrada para esse driver ODBC. Esse valor não pode ser localizado.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Arquivo\_
</dt> <dd>

O arquivo DLL para drivers listados na coluna Driver. A coluna \_ Arquivo é uma chave externa na tabela [Arquivo](file-table.md). O nome do arquivo inserido na coluna Nome do arquivo desse registro da tabela arquivo deve estar no formato de nome de arquivo curto. A sintaxe \| LFN do SFN não pode ser usada.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuração de \_ arquivo
</dt> <dd>

O arquivo DLL de instalação para o driver se ele for diferente do Driver. A coluna \_ Arquivo é uma chave externa na tabela [Arquivo](file-table.md). O nome do arquivo inserido na coluna Nome do arquivo desse registro da tabela arquivo deve estar no formato de nome de arquivo curto. A sintaxe \| LFN do SFN não pode ser usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

As [ações InstallODBC](installodbc-action.md) [e RemoveODBC](removeodbc-action.md) em [*tabelas de*](s-gly.md) sequência processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência,* [consulte Usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



