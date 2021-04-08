---
description: O instalador mantém informações sobre a estrutura do diretório de instalação na tabela de diretórios.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Especificando a estrutura do diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827284"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="4f2de-103">Especificando a estrutura do diretório</span><span class="sxs-lookup"><span data-stu-id="4f2de-103">Specifying Directory Structure</span></span>

<span data-ttu-id="4f2de-104">O instalador mantém informações sobre a estrutura do diretório de instalação na [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f2de-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="4f2de-105">Consulte o [grupo tabelas principais](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="4f2de-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="4f2de-106">Nesta seção, você adiciona informações de estrutura de diretório para o exemplo do bloco de notas ao banco de dados vazio que você criou na [importação de um banco de dados em branco](importing-a-blank-database.md).</span><span class="sxs-lookup"><span data-stu-id="4f2de-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="4f2de-107">Use o editor de banco de dados Orca fornecido com o SDK ou outro editor para abrir a tabela de diretórios no MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="4f2de-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="4f2de-108">Use o editor para inserir os dados a seguir na tabela de diretório em branco.</span><span class="sxs-lookup"><span data-stu-id="4f2de-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="4f2de-109">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="4f2de-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="4f2de-110">Diretório</span><span class="sxs-lookup"><span data-stu-id="4f2de-110">Directory</span></span>                                        | <span data-ttu-id="4f2de-111">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="4f2de-111">Directory\_Parent</span></span>                                | <span data-ttu-id="4f2de-112">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="4f2de-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="4f2de-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="4f2de-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="4f2de-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="4f2de-114">SourceDir</span></span>         |
| [<span data-ttu-id="4f2de-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="4f2de-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="4f2de-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="4f2de-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="4f2de-117">.</span><span class="sxs-lookup"><span data-stu-id="4f2de-117">.</span></span>                 |
| <span data-ttu-id="4f2de-118">ARTSDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-118">ARTSDIR</span></span>                                          | <span data-ttu-id="4f2de-119">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="4f2de-120">Artes: eventos</span><span class="sxs-lookup"><span data-stu-id="4f2de-120">Arts:Events</span></span>       |
| <span data-ttu-id="4f2de-121">HOLDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-121">HOLDIR</span></span>                                           | <span data-ttu-id="4f2de-122">MONDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-122">MONDIR</span></span>                                           | <span data-ttu-id="4f2de-123">.: Feriados</span><span class="sxs-lookup"><span data-stu-id="4f2de-123">.:Holidays</span></span>        |
| <span data-ttu-id="4f2de-124">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-124">MENUDIR</span></span>                                          | <span data-ttu-id="4f2de-125">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="4f2de-126">Menu</span><span class="sxs-lookup"><span data-stu-id="4f2de-126">Menu</span></span>              |
| <span data-ttu-id="4f2de-127">MONDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-127">MONDIR</span></span>                                           | <span data-ttu-id="4f2de-128">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="4f2de-129">Check</span><span class="sxs-lookup"><span data-stu-id="4f2de-129">Gate</span></span>              |
| <span data-ttu-id="4f2de-130">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="4f2de-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="4f2de-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="4f2de-132">\_Parque vermelho: bloco de notas</span><span class="sxs-lookup"><span data-stu-id="4f2de-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="4f2de-133">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-133">SPORTDIR</span></span>                                         | <span data-ttu-id="4f2de-134">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="4f2de-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="4f2de-135">Esportes: eventos</span><span class="sxs-lookup"><span data-stu-id="4f2de-135">Sports:Events</span></span>     |



 

<span data-ttu-id="4f2de-136">A inserção desses dados na tabela de diretórios especifica as estruturas de diretório de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="4f2de-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="4f2de-137">Consulte a [tabela de diretórios](directory-table.md) e [usando os tópicos da tabela de diretórios](using-the-directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4f2de-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="4f2de-138">Observe que a propriedade [**TARGETDIR**](targetdir.md) deve ser o nome de uma raiz na tabela de diretórios de cada instalação.</span><span class="sxs-lookup"><span data-stu-id="4f2de-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="4f2de-139">Continuar</span><span class="sxs-lookup"><span data-stu-id="4f2de-139">Continue</span></span>](specifying-components.md)

 

 



