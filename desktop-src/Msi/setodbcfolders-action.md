---
description: A ação SetODBCFolders verifica se há drivers ODBC existentes no sistema e define o diretório de destino de cada novo driver para o local de um driver existente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Ação SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceaefc2e9722b82ab0753c46b9e1e85a0ab3628a83b9f3abe66cf183c543fbe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628636"
---
# <a name="setodbcfolders-action"></a>Ação SetODBCFolders

A ação SetODBCFolders verifica se há drivers ODBC existentes no sistema e define o diretório de destino de cada novo driver para o local de um driver existente.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação SetODBCFolders deve vir após a [ação CostFinalize](costfinalize-action.md) e antes da [ação InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Descrição do driver. A chave do driver ODBC.                                            |
| \[2\] | Local da pasta original do novo driver.                                         |
| \[3\] | Novo local de pasta para o novo driver. Esse é o local de um driver existente. |



 

## <a name="remarks"></a>Comentários

Essa ação coloca um novo driver no mesmo diretório que o driver existente que está sendo substituído. A ação SetODBCFolders usa a [tabela Directory](directory-table.md) para definir os locais dos drivers existentes que devem ser substituídos.

 

 



