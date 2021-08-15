---
description: A tabela ODBCTranslator lista os conversores ODBC que pertencem à instalação.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabela ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd59c535963b3c42e94c8c904d448540072913b56bedb58c3e0bddc72dd6c6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942887"
---
# <a name="odbctranslator-table"></a>Tabela ODBCTranslator

A tabela ODBCTranslator lista os conversores ODBC que pertencem à instalação.

A tabela ODBCTranslator tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Tradutor  | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Descrição | [Text](text.md)             | N   | N        |
| Arquivo\_      | [Identificador](identifier.md) | N   | N        |
| Configuração de arquivo \_ | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Tradutor
</dt> <dd>

Nome do token interno para o tradutor. Uma chave primária para a tabela.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na tabela de componentes.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

A descrição registrada para este conversor de driver ODBC. Este valor não pode ser localizado.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

o arquivo DLL para a transferência listada na coluna Tradutor. A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md). O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto. A \| sintaxe SFN LFN não pode ser usada.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuração de arquivo \_
</dt> <dd>

o arquivo DLL de instalação para o tradutor se ele for diferente da coluna Tradutor. A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md). O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto. A \| sintaxe SFN LFN não pode ser usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



