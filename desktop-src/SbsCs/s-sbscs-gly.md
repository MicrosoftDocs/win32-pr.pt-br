---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: S (aplicativos isolados e assemblies lado a lado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663002"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="278c0-103">S (aplicativos isolados e assemblies lado a lado)</span><span class="sxs-lookup"><span data-stu-id="278c0-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="278c0-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="278c0-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="278c0-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly lado a lado compartilhado**</span><span class="sxs-lookup"><span data-stu-id="278c0-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="278c0-106">Um assembly compartilhado lado a lado está disponível para uso por vários aplicativos no computador.</span><span class="sxs-lookup"><span data-stu-id="278c0-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="278c0-107">Ele é instalado na pasta WinSxS do diretório do Windows.</span><span class="sxs-lookup"><span data-stu-id="278c0-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="278c0-108">Os aplicativos e administradores podem gerenciar a versão de um assembly compartilhado a ser usado especificando a configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="278c0-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="278c0-109">Os assemblies lado a lado são sempre acompanhados por arquivos de manifesto que fornecem informações sobre o assembly para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="278c0-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="278c0-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly lado a lado**</span><span class="sxs-lookup"><span data-stu-id="278c0-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="278c0-111">Um assembly lado a lado é um assembly do Win32 acompanhado por manifestos.</span><span class="sxs-lookup"><span data-stu-id="278c0-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="278c0-112">Um assembly lado a lado contém uma coleção de recursos — um grupo de DLLs, classes do Windows, servidores COM, bibliotecas de tipos ou interfaces — que são sempre fornecidos para aplicativos juntos.</span><span class="sxs-lookup"><span data-stu-id="278c0-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="278c0-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**compartilhamento de assembly lado a lado**</span><span class="sxs-lookup"><span data-stu-id="278c0-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="278c0-114">Uso de assemblies lado a lado para compartilhar com segurança assemblies entre vários aplicativos e para deslocar os efeitos negativos de compartilhamento, como conflitos de DLL.</span><span class="sxs-lookup"><span data-stu-id="278c0-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="278c0-115">Em vez de ter uma única versão de um assembly que assume compatibilidade com versões anteriores com todos os aplicativos, o compartilhamento de assembly lado a lado permite que várias versões de um assembly Win32 sejam executadas simultaneamente no sistema.</span><span class="sxs-lookup"><span data-stu-id="278c0-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="278c0-116">Os assemblies lado a lado são sempre acompanhados por arquivos de manifesto de assembly que fornecem informações sobre o assembly para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="278c0-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="278c0-117">Os aplicativos e administradores podem gerenciar o compartilhamento de assembly lado a lado após a implantação atualizando a configuração do aplicativo em uma base global ou por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="278c0-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



