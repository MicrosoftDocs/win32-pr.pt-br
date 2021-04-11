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
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="e5390-103">Obtendo um identificador de banco de dados</span><span class="sxs-lookup"><span data-stu-id="e5390-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="e5390-104">Antes de trabalhar com um banco de dados, você deve primeiro obter um identificador para ele.</span><span class="sxs-lookup"><span data-stu-id="e5390-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="e5390-105">**Para acessar informações sobre um banco de dados do instalador**</span><span class="sxs-lookup"><span data-stu-id="e5390-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="e5390-106">Obtenha um identificador para o banco de dados de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="e5390-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="e5390-107">Se uma instalação estiver em andamento, obtenha um identificador para o banco de dados ativo chamando a função [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .</span><span class="sxs-lookup"><span data-stu-id="e5390-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="e5390-108">Se uma instalação não estiver em andamento, abra qualquer banco de dados especificado chamando a função [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .</span><span class="sxs-lookup"><span data-stu-id="e5390-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="e5390-109">Depois que o banco de dados tiver sido aberto, você poderá chamar funções para obter informações sobre o banco de dados ou para manipular o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e5390-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="e5390-110">Crie um objeto **View** e especifique uma consulta SQL do banco de dados aberto chamando a função [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="e5390-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="e5390-111">Obtenha um registro que contém todas as chaves primárias de uma tabela especificada no banco de dados aberto chamando a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .</span><span class="sxs-lookup"><span data-stu-id="e5390-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="e5390-112">Verifique o estado atual de um banco de dados aberto chamando a função [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) .</span><span class="sxs-lookup"><span data-stu-id="e5390-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="e5390-113">Com a função **MsiGetDatabaseState** , você pode determinar o status de leitura/gravação de um banco de dados ou se o identificador é válido.</span><span class="sxs-lookup"><span data-stu-id="e5390-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



