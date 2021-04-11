---
description: As tabelas do grupo tabelas do sistema controlam as tabelas e colunas do banco de dados de instalação.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo de tabelas do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090931"
---
# <a name="system-tables-group"></a><span data-ttu-id="6829c-103">Grupo de tabelas do sistema</span><span class="sxs-lookup"><span data-stu-id="6829c-103">System Tables Group</span></span>

<span data-ttu-id="6829c-104">As tabelas do grupo tabelas do sistema controlam as tabelas e colunas do banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="6829c-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="6829c-105">A [ \_ tabela tabelas](-tables-table.md) controla todas as tabelas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6829c-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="6829c-106">Isso inclui tabelas que você pode ter criado para suas próprias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6829c-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="6829c-107">Consulte esta tabela para descobrir se existe uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6829c-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="6829c-108">A [ \_ tabela Columns](-columns-table.md) controla as colunas no banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="6829c-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="6829c-109">As colunas temporárias não são rastreadas atualmente por esta tabela.</span><span class="sxs-lookup"><span data-stu-id="6829c-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="6829c-110">Consulte esta tabela para saber se existe uma determinada coluna.</span><span class="sxs-lookup"><span data-stu-id="6829c-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="6829c-111">A [ \_ tabela de fluxos](-streams-table.md) lista os fluxos de dados OLE inseridos.</span><span class="sxs-lookup"><span data-stu-id="6829c-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="6829c-112">A [ \_ tabela de armazenamentos](-storages-table.md) lista armazenamentos de dados OLE inseridos.</span><span class="sxs-lookup"><span data-stu-id="6829c-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="6829c-113">A [ \_ tabela de validação](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="6829c-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="6829c-114">A \_ tabela de validação controla os tipos e os intervalos permitidos de cada coluna no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6829c-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="6829c-115">A \_ tabela de validação é usada durante o processo de validação do banco de dados para garantir que todas as colunas sejam contadas e tenham os valores corretos.</span><span class="sxs-lookup"><span data-stu-id="6829c-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="6829c-116">Esta tabela não é enviada com o banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="6829c-116">This table is not shipped with the installer database.</span></span>

 

 



