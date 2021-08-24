---
description: A ação RemoveODBC remove as fontes de dados, os tradutores e os drivers listados para remoção durante a instalação.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Ação RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6619bc5b8a18cff2ee33dbe45261764c682953bad75a17cb9d6e93cbe487147b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580426"
---
# <a name="removeodbc-action"></a>Ação RemoveODBC

A ação RemoveODBC remove as fontes de dados, os tradutores e os drivers listados para remoção durante a instalação. Essa ação consulta a tabela [ODBCDataSource](odbcdatasource-table.md), a tabela [ODBCTranslator](odbctranslator-table.md)e a [tabela ODBCDriver](odbcdriver-table.md) para cada fonte de dados, tradutor ou driver agendado para remoção.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Para cada driver instalado.



| Campo | Descrição dos dados de ação               |
|-------|------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC. |
| \[2\] | Componentid                              |



 

Para cada tradutor instalado.



| Campo | Descrição dos dados de ação               |
|-------|------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC. |
| \[2\] | Componentid                              |



 

Para cada fonte de dados instalada.



| Campo | Descrição dos dados de ação                              |
|-------|---------------------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC.                |
| \[2\] | Componentid                                             |
| \[3\] | Registro: SQL \_ REMOVER \_ DSN ou SQL \_ REMOVE \_ SYS \_ DSN |



 

## <a name="remarks"></a>Comentários

Se a contagem de uso ODBC e a contagem de uso do arquivo se tornarem zero, o arquivo será removido. O registro depende das contagens de uso ODBC e a remoção de arquivos é baseada em contagens de referência de chave de DLLs compartilhadas.

 

 



