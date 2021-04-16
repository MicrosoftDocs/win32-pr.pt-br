---
description: A ação SetODBCFolders verifica os drivers ODBC existentes no sistema e define o diretório de destino de cada novo driver para o local de um driver existente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Ação SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758763"
---
# <a name="setodbcfolders-action"></a>Ação SetODBCFolders

A ação SetODBCFolders verifica os drivers ODBC existentes no sistema e define o diretório de destino de cada novo driver para o local de um driver existente.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação SetODBCFolders deve vir após a [ação CostFinalize](costfinalize-action.md) e antes da [ação InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC.                                            |
| \[2\] | Local da pasta original do novo driver.                                         |
| \[3\] | Novo local da pasta para o novo driver. Este é o local de um driver existente. |



 

## <a name="remarks"></a>Comentários

Essa ação coloca um novo driver no mesmo diretório que o driver existente que está sendo substituído. A ação SetODBCFolders usa a [tabela de diretórios](directory-table.md) para definir os locais dos drivers existentes que serão substituídos.

 

 



