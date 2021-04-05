---
description: Um assembly Win32 pode ser instalado como um assembly compartilhado e estar disponível para uso por vários aplicativos no computador. Os assemblies compartilhados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662592"
---
# <a name="shared-assemblies"></a><span data-ttu-id="c44cc-104">Assemblies compartilhados</span><span class="sxs-lookup"><span data-stu-id="c44cc-104">Shared Assemblies</span></span>

<span data-ttu-id="c44cc-105">Um assembly Win32 pode ser instalado como um assembly compartilhado e estar disponível para uso por vários aplicativos no computador.</span><span class="sxs-lookup"><span data-stu-id="c44cc-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="c44cc-106">Os assemblies compartilhados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44cc-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="c44cc-107">Os assemblies compartilhados são instalados como [assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="c44cc-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="c44cc-108">O Windows Installer instala assemblies compartilhados lado a lado na pasta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="c44cc-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="c44cc-109">Os assemblies não são registrados globalmente no sistema, mas estão globalmente disponíveis para qualquer aplicativo que especifique uma dependência no assembly em um arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="c44cc-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="c44cc-110">Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c44cc-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="c44cc-111">Em sistemas operacionais anteriores ao Windows XP, os assemblies compartilhados geralmente são instalados na pasta do sistema do Windows e registrados globalmente.</span><span class="sxs-lookup"><span data-stu-id="c44cc-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="c44cc-112">A versão mais recente instalada está disponível para qualquer aplicativo associado a ele.</span><span class="sxs-lookup"><span data-stu-id="c44cc-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="c44cc-113">Para obter informações sobre como criar um pacote de Windows Installer para instalar um assembly compartilhado, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c44cc-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="c44cc-114">Instalando assemblies do Win32 para compartilhamento lado a lado no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c44cc-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="c44cc-115">Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c44cc-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
