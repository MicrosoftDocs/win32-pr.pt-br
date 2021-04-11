---
description: O Windows Installer determina se deve permitir a remoção de um assembly de Common Language Runtime com base em uma lista de clientes que ele mantém independentemente do assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Remoção de assemblies do cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169521"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="d0006-103">Remoção de assemblies do cache de assembly global</span><span class="sxs-lookup"><span data-stu-id="d0006-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="d0006-104">O Windows Installer determina se deve permitir a remoção de um assembly de Common Language Runtime com base em uma lista de clientes que ele mantém independentemente do assembly.</span><span class="sxs-lookup"><span data-stu-id="d0006-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="d0006-105">O Windows Installer mantém um bit PIN para representar Windows Installer clientes do assembly.</span><span class="sxs-lookup"><span data-stu-id="d0006-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="d0006-106">O instalador fixa o assembly para o primeiro cliente Windows Installer e o desafixa quando o último cliente Windows Installer é removido.</span><span class="sxs-lookup"><span data-stu-id="d0006-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="d0006-107">O assembly mantém um bit de PIN para cada cliente de um assembly.</span><span class="sxs-lookup"><span data-stu-id="d0006-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="d0006-108">O Windows Installer não é diretamente responsável pela remoção física de assemblies de Common Language Runtime do computador.</span><span class="sxs-lookup"><span data-stu-id="d0006-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="d0006-109">O instalador desafixa o assembly quando o último cliente de Windows Installer é removido.</span><span class="sxs-lookup"><span data-stu-id="d0006-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="d0006-110">Se o Windows Installer for o último cliente do assembly, o Common Language Runtime fornecerá a opção de forçar uma limpeza síncrona do assembly.</span><span class="sxs-lookup"><span data-stu-id="d0006-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="d0006-111">O processo de limpeza é atômico e não há nenhuma provisão para uma "reversão" neste ponto.</span><span class="sxs-lookup"><span data-stu-id="d0006-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="d0006-112">Toda a desanexação de assemblies de Common Language Runtime deve ocorrer depois que o usuário tiver a oportunidade de cancelar a instalação ou remoção.</span><span class="sxs-lookup"><span data-stu-id="d0006-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



