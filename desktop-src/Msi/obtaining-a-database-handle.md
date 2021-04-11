---
description: Antes de trabalhar com um banco de dados, você deve primeiro obter um identificador para ele.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Obtendo um identificador de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091016"
---
# <a name="obtaining-a-database-handle"></a>Obtendo um identificador de banco de dados

Antes de trabalhar com um banco de dados, você deve primeiro obter um identificador para ele.

**Para acessar informações sobre um banco de dados do instalador**

1.  Obtenha um identificador para o banco de dados de uma das duas maneiras:
    -   Se uma instalação estiver em andamento, obtenha um identificador para o banco de dados ativo chamando a função [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .
    -   Se uma instalação não estiver em andamento, abra qualquer banco de dados especificado chamando a função [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .
2.  Depois que o banco de dados tiver sido aberto, você poderá chamar funções para obter informações sobre o banco de dados ou para manipular o banco de dados.
    -   Crie um objeto **View** e especifique uma consulta SQL do banco de dados aberto chamando a função [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .
    -   Obtenha um registro que contém todas as chaves primárias de uma tabela especificada no banco de dados aberto chamando a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .
    -   Verifique o estado atual de um banco de dados aberto chamando a função [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) . Com a função **MsiGetDatabaseState** , você pode determinar o status de leitura/gravação de um banco de dados ou se o identificador é válido.

 

 



