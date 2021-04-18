---
description: O banco de dados do instalador permite que o desenvolvedor de um pacote de instalação controle a transferência de um aplicativo de uma origem para uma imagem de destino.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Usando o banco de dados do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778555"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="e7e22-103">Usando o banco de dados do instalador</span><span class="sxs-lookup"><span data-stu-id="e7e22-103">Using the Installer Database</span></span>

<span data-ttu-id="e7e22-104">O [banco de dados do instalador](installer-database.md) permite que o desenvolvedor de um pacote de instalação controle a transferência de um aplicativo de uma origem para uma imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e22-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="e7e22-105">O layout das imagens de origem e de destino do aplicativo é especificado na tabela de [diretórios](directory-table.md) e as ações que instalam o aplicativo são especificadas em seis tabelas de sequência:</span><span class="sxs-lookup"><span data-stu-id="e7e22-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="e7e22-106">Tabela [InstallUISequence](installuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="e7e22-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="e7e22-107">Tabela [InstallExecuteSequence](installexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="e7e22-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="e7e22-108">Tabela [AdminUISequence](adminuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="e7e22-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="e7e22-109">Tabela [AdminExecuteSequence](adminexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="e7e22-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="e7e22-110">Tabela [AdvtUISequence](advtuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="e7e22-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="e7e22-111">Tabela [AdvtExecuteSequence](advtexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="e7e22-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="e7e22-112">As seções a seguir descrevem como usar o [banco de dados do instalador](installer-database.md):</span><span class="sxs-lookup"><span data-stu-id="e7e22-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="e7e22-113">Usando a tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="e7e22-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="e7e22-114">Usando uma tabela de sequência</span><span class="sxs-lookup"><span data-stu-id="e7e22-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="e7e22-115">Obtendo um identificador de banco de dados</span><span class="sxs-lookup"><span data-stu-id="e7e22-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="e7e22-116">Confirmando bancos de dados</span><span class="sxs-lookup"><span data-stu-id="e7e22-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="e7e22-117">Importando e exportando</span><span class="sxs-lookup"><span data-stu-id="e7e22-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="e7e22-118">Mesclando bancos de dados</span><span class="sxs-lookup"><span data-stu-id="e7e22-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="e7e22-119">Nomeando tabelas, propriedades e ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="e7e22-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="e7e22-120">Limitações de OLE em fluxos</span><span class="sxs-lookup"><span data-stu-id="e7e22-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="e7e22-121">Trabalhando com consultas</span><span class="sxs-lookup"><span data-stu-id="e7e22-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="e7e22-122">Adicionando dados binários a uma tabela usando SQL</span><span class="sxs-lookup"><span data-stu-id="e7e22-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="e7e22-123">Trabalhando com registros</span><span class="sxs-lookup"><span data-stu-id="e7e22-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="e7e22-124">Trabalhando com locais de pasta</span><span class="sxs-lookup"><span data-stu-id="e7e22-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="e7e22-125">Especificando a ordem de auto-registro</span><span class="sxs-lookup"><span data-stu-id="e7e22-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="e7e22-126">Ações de condicionamento a serem executadas durante a remoção</span><span class="sxs-lookup"><span data-stu-id="e7e22-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="e7e22-127">Chamando funções de banco de dados de programas</span><span class="sxs-lookup"><span data-stu-id="e7e22-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="e7e22-128">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="e7e22-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="e7e22-129">Formato de definição de coluna</span><span class="sxs-lookup"><span data-stu-id="e7e22-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="e7e22-130">Determinando se uma coluna é uma chave primária ou externa</span><span class="sxs-lookup"><span data-stu-id="e7e22-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



