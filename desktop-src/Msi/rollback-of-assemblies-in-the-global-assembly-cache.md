---
description: Um processo de duas etapas estende o modelo de transação do Windows Installer para os produtos que contêm Common Language Runtime assemblies. Isso permite que o instalador reverta instalações e remoções de assemblies malsucedidas.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reversão de assemblies no cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647054"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="5bd3e-104">Reversão de assemblies no cache de assembly global</span><span class="sxs-lookup"><span data-stu-id="5bd3e-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="5bd3e-105">Um processo de duas etapas estende o modelo de transação do Windows Installer para os produtos que contêm Common Language Runtime assemblies.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="5bd3e-106">Isso permite que o instalador reverta instalações e remoções de assemblies malsucedidas.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="5bd3e-107">Durante a primeira etapa, o Windows Installer usa a estrutura de Microsoft .NET para criar uma interface para cada assembly.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="5bd3e-108">O Windows Installer usa tantas interfaces quanto há assemblies sendo instalados.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="5bd3e-109">A confirmação de um assembly usando apenas uma dessas interfaces significa que o assembly está pronto para substituir qualquer assembly existente com o mesmo nome, mas ainda não o substitui.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="5bd3e-110">Se o usuário cancelar a instalação ou se houver um erro fatal de instalação, o Windows Installer ainda poderá reverter o assembly para seu estado anterior, liberando essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="5bd3e-111">Depois que o Windows Installer concluir a instalação de todos os assemblies e componentes de Windows Installer, o instalador poderá iniciar a segunda etapa da instalação.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="5bd3e-112">A segunda etapa usa uma função separada para fazer a confirmação final de todos os novos assemblies de Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="5bd3e-113">Isso substitui todos os assemblies existentes com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-113">This replaces any existing assemblies with the same name.</span></span>

 

 



