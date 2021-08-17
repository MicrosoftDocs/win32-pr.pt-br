---
description: Antes de trabalhar com um banco de dados, você deve primeiro obter um handle para ele.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Obtendo um guidão de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a325c7c69bed4141de8f553a344b20b5f3c61bfe28a1594105c0a853b7075744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145559"
---
# <a name="obtaining-a-database-handle"></a>Obtendo um guidão de banco de dados

Antes de trabalhar com um banco de dados, você deve primeiro obter um handle para ele.

**Para acessar informações sobre um banco de dados do instalador**

1.  Obtenha um handle para o banco de dados de uma das duas maneiras:
    -   Se uma instalação estiver em andamento, obter um handle para o banco de dados ativo chamando a [**função MsiGetActiveDatabase.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)
    -   Se uma instalação não estiver em andamento, abra qualquer banco de dados especificado chamando a [**função MsiOpenDatabase.**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
2.  Depois que o banco de dados tiver sido aberto, você poderá chamar funções para obter informações sobre o banco de dados ou manipular o banco de dados.
    -   Crie um **objeto View** e especifique SQL consulta do banco de dados aberto chamando a [**função MsiDatabaseOpenView.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)
    -   Obtenha um registro que contém todas as chaves primárias de uma tabela especificada no banco de dados aberto chamando a [**função MsiDatabaseGetPrimaryKeys.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)
    -   Verifique o estado atual de um banco de dados aberto chamando a [**função MsiGetDatabaseState.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) Com a **função MsiGetDatabaseState,** você pode determinar o status de leitura/gravação de um banco de dados ou se o handle é válido.

 

 



