---
description: A ação RemoveODBC remove as fontes de dados, os tradutores e os drivers listados para remoção durante a instalação.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Ação RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787496"
---
# <a name="removeodbc-action"></a>Ação RemoveODBC

A ação RemoveODBC remove as fontes de dados, os tradutores e os drivers listados para remoção durante a instalação. Essa ação consulta a tabela [ODBCDataSource](odbcdatasource-table.md), a [tabela ODBCTranslator](odbctranslator-table.md)e a [tabela ODBCDriver](odbcdriver-table.md) para cada fonte de dados, Tradutor ou driver agendado para remoção.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Para cada driver instalado.



| Campo | Descrição dos dados da ação               |
|-------|------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC. |
| \[2\] | ComponentId                              |



 

Para cada tradutor instalado.



| Campo | Descrição dos dados da ação               |
|-------|------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC. |
| \[2\] | ComponentId                              |



 

Para cada fonte de dados instalada.



| Campo | Descrição dos dados da ação                              |
|-------|---------------------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC.                |
| \[2\] | ComponentId                                             |
| \[3\] | Registro: SQL \_ Remove \_ DSN ou SQL \_ Remove \_ Sys \_ DSN |



 

## <a name="remarks"></a>Comentários

Se a contagem de uso do ODBC e a contagem de uso do arquivo se tornarem zero, o arquivo será removido. O registro depende de contagens de uso de ODBC e a remoção de arquivo é baseada em contagens de referência de chave de DLLs compartilhadas.

 

 



