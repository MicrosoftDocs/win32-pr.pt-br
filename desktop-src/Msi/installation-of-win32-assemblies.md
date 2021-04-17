---
description: Instale os assemblies do Win32 tornando-os um componente do pacote Microsoft Windows Installer que instala ou atualiza seu aplicativo.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalação de assemblies Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749796"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="15ca3-103">Instalação de assemblies Win32</span><span class="sxs-lookup"><span data-stu-id="15ca3-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="15ca3-104">Instale os assemblies do Win32 tornando-os um componente do pacote Microsoft Windows Installer que instala ou atualiza seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15ca3-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="15ca3-105">Quando você cria a [tabela MsiAssembly](msiassembly-table.md) e a [tabela MsiAssemblyName](msiassemblyname-table.md), isso identifica o componente na \_ coluna componente como um assembly.</span><span class="sxs-lookup"><span data-stu-id="15ca3-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="15ca3-106">O instalador definirá a propriedade [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) para a versão de arquivo do Sxs.dll em sistemas operacionais que podem dar suporte a assemblies Win32 e não definir essa propriedade de outra forma.</span><span class="sxs-lookup"><span data-stu-id="15ca3-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="15ca3-107">No Windows Vista e no Windows XP, Windows Installer não grava informações de assembly no registro.</span><span class="sxs-lookup"><span data-stu-id="15ca3-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="15ca3-108">Além disso, assemblies compartilhados, assemblies privados e assemblies lado a lado podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="15ca3-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="15ca3-109">Para obter informações, consulte [assemblies compartilhados](shared-assemblies.md), [assemblies privados](private-assemblies.md)e [assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="15ca3-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="15ca3-110">As seções a seguir descrevem como criar um pacote de Windows Installer para instalar assemblies do Win32 como compartilhado, privado ou lado a lado em sistemas operacionais Windows diferentes.</span><span class="sxs-lookup"><span data-stu-id="15ca3-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="15ca3-111">Instalando assemblies do Win32 para compartilhamento lado a lado no Windows XP</span><span class="sxs-lookup"><span data-stu-id="15ca3-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="15ca3-112">Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP</span><span class="sxs-lookup"><span data-stu-id="15ca3-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



