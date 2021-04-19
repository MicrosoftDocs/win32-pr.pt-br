---
description: Os assemblies do Common Language Runtime instalados no cache de assembly global devem ter arquivos idênticos em todas as ocorrências do assembly.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modos de reinstalação de assemblies do Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768463"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="eeb24-103">Modos de reinstalação de assemblies do Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="eeb24-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="eeb24-104">Os assemblies do Common Language Runtime instalados no cache de assembly global devem ter arquivos idênticos em todas as ocorrências do assembly.</span><span class="sxs-lookup"><span data-stu-id="eeb24-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="eeb24-105">Isso significa que os modos de reinstalação usados por [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) e [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) devem ter significados diferentes para componentes regulares e Common Language Runtime assemblies.</span><span class="sxs-lookup"><span data-stu-id="eeb24-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="eeb24-106">As definições a seguir dos modos de reinstalação se aplicam a assemblies Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="eeb24-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="eeb24-107">Modo de reinstalação</span><span class="sxs-lookup"><span data-stu-id="eeb24-107">Reinstall mode</span></span>                  | <span data-ttu-id="eeb24-108">Significado para componentes de Microsoft .NET</span><span class="sxs-lookup"><span data-stu-id="eeb24-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb24-109">reinstalação de \_ filemission</span><span class="sxs-lookup"><span data-stu-id="eeb24-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="eeb24-110">Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.</span><span class="sxs-lookup"><span data-stu-id="eeb24-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="eeb24-111">reinstalar o \_ FILEOLDERVERSION</span><span class="sxs-lookup"><span data-stu-id="eeb24-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="eeb24-112">Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.</span><span class="sxs-lookup"><span data-stu-id="eeb24-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="eeb24-113">reinstalar o \_ FILEEQUALVERSION</span><span class="sxs-lookup"><span data-stu-id="eeb24-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="eeb24-114">Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.</span><span class="sxs-lookup"><span data-stu-id="eeb24-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="eeb24-115">reinstalar o \_ FILEexato</span><span class="sxs-lookup"><span data-stu-id="eeb24-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="eeb24-116">Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.</span><span class="sxs-lookup"><span data-stu-id="eeb24-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="eeb24-117">reinstalar o \_ FILEverify</span><span class="sxs-lookup"><span data-stu-id="eeb24-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="eeb24-118">Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou se o componente existente estiver incompleto ou corrompido.</span><span class="sxs-lookup"><span data-stu-id="eeb24-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="eeb24-119">reinstalar o \_ FILEreplace</span><span class="sxs-lookup"><span data-stu-id="eeb24-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="eeb24-120">Sempre instale ou reinstale o componente Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="eeb24-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



