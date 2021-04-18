---
description: Siga estas diretrizes para facilitar a localização de pacotes de Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparando um pacote de Windows Installer para localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752842"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="cddd5-103">Preparando um pacote de Windows Installer para localização</span><span class="sxs-lookup"><span data-stu-id="cddd5-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="cddd5-104">A localização de um pacote de Windows Installer em vários idiomas pode ser bastante facilitada fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cddd5-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="cddd5-105">Crie um banco de dados de instalação base que seja uma página de código neutra.</span><span class="sxs-lookup"><span data-stu-id="cddd5-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="cddd5-106">Consulte [criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="cddd5-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="cddd5-107">A página de código do banco de dados localizado pode ser definida importando uma tabela de arquivamento de texto com uma página de código não neutra no banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="cddd5-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="cddd5-108">Consulte [Configurando a página de código de um banco de dados](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="cddd5-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="cddd5-109">Organize arquivos que exigem localização em componentes separados e instale esses arquivos em diretórios separados.</span><span class="sxs-lookup"><span data-stu-id="cddd5-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="cddd5-110">Isso garante que dois pacotes localizados nunca instalem arquivos com nomes idênticos no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="cddd5-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="cddd5-111">Por exemplo, um aplicativo em todo o mundo usando os recursos a seguir pode ter três componentes.</span><span class="sxs-lookup"><span data-stu-id="cddd5-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="cddd5-112">Componente</span><span class="sxs-lookup"><span data-stu-id="cddd5-112">Component</span></span> | <span data-ttu-id="cddd5-113">Recurso</span><span class="sxs-lookup"><span data-stu-id="cddd5-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="cddd5-114">PAÍSES</span><span class="sxs-lookup"><span data-stu-id="cddd5-114">WORLD</span></span>     | <span data-ttu-id="cddd5-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="cddd5-115">worldwide.exe</span></span>              |
| <span data-ttu-id="cddd5-116">PAÍSES</span><span class="sxs-lookup"><span data-stu-id="cddd5-116">WORLD</span></span>     | <span data-ttu-id="cddd5-117">entradas de registro mundiais</span><span class="sxs-lookup"><span data-stu-id="cddd5-117">worldwide registry entries</span></span> |
| <span data-ttu-id="cddd5-118">PAÍSES</span><span class="sxs-lookup"><span data-stu-id="cddd5-118">WORLD</span></span>     | <span data-ttu-id="cddd5-119">atalho mundial</span><span class="sxs-lookup"><span data-stu-id="cddd5-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="cddd5-120">ENG</span><span class="sxs-lookup"><span data-stu-id="cddd5-120">ENG</span></span>       | <span data-ttu-id="cddd5-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="cddd5-121">engui.dll</span></span>                  |
| <span data-ttu-id="cddd5-122">ENG</span><span class="sxs-lookup"><span data-stu-id="cddd5-122">ENG</span></span>       | <span data-ttu-id="cddd5-123">readme.txt</span><span class="sxs-lookup"><span data-stu-id="cddd5-123">readme.txt</span></span>                 |
| <span data-ttu-id="cddd5-124">FRA</span><span class="sxs-lookup"><span data-stu-id="cddd5-124">FRA</span></span>       | <span data-ttu-id="cddd5-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="cddd5-125">fraui.dll</span></span>                  |
| <span data-ttu-id="cddd5-126">FRA</span><span class="sxs-lookup"><span data-stu-id="cddd5-126">FRA</span></span>       | <span data-ttu-id="cddd5-127">readme.txt</span><span class="sxs-lookup"><span data-stu-id="cddd5-127">readme.txt</span></span>                 |



 

<span data-ttu-id="cddd5-128">Os arquivos que precisam ser localizados podem ser instalados nos seguintes locais de diretório:</span><span class="sxs-lookup"><span data-stu-id="cddd5-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="cddd5-129">\[ProgramFilesFolder \] \\ mundo \\worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="cddd5-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="cddd5-130">\[ProgramFilesFolder \] \\ mundial \\ em inglês \\engui.dll</span><span class="sxs-lookup"><span data-stu-id="cddd5-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="cddd5-131">\[ProgramFilesFolder \] \\ mundial \\ em inglês \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="cddd5-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="cddd5-132">\[fraui.dll ProgramFilesFolder do \] \\ mundo \\ francês \\</span><span class="sxs-lookup"><span data-stu-id="cddd5-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="cddd5-133">\[readme.txt ProgramFilesFolder do \] \\ mundo \\ francês \\</span><span class="sxs-lookup"><span data-stu-id="cddd5-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



