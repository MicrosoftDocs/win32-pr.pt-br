---
description: Windows Installer pode instalar, remover e atualizar assemblies do Win32 e assemblies usados pelo Common Language Runtime da estrutura de Microsoft .NET.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757131"
---
# <a name="assemblies"></a><span data-ttu-id="bb9cd-103">Assemblies</span><span class="sxs-lookup"><span data-stu-id="bb9cd-103">Assemblies</span></span>

<span data-ttu-id="bb9cd-104">Windows Installer pode instalar, remover e atualizar assemblies do Win32 e assemblies usados pelo Common Language Runtime da estrutura de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="bb9cd-105">Um assembly é manipulado pelo Windows Installer como um único componente de instalador.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="bb9cd-106">Todos os arquivos que constituem um assembly devem estar contidos em um único componente de instalador listado na tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9cd-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="bb9cd-107">Windows Installer em execução no Windows Vista e no Windows XP podem instalar assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="bb9cd-108">Os assemblies lado a lado podem compartilhar com segurança assemblies entre vários aplicativos e podem deslocar os efeitos negativos do compartilhamento de assembly, como conflitos de DLL.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="bb9cd-109">Em vez de uma única versão de um assembly que assume compatibilidade com versões anteriores com todos os aplicativos, o compartilhamento de assembly lado a lado permite que várias versões de um assembly COM ou Win32 sejam executadas simultaneamente no sistema.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="bb9cd-110">Esse recurso aprimorado para isolar aplicativos é uma parte importante da estrutura de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="bb9cd-111">Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span><span class="sxs-lookup"><span data-stu-id="bb9cd-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="bb9cd-112">As seções a seguir descrevem o uso de assemblies com o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bb9cd-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="bb9cd-113">Adicionando assemblies a um pacote</span><span class="sxs-lookup"><span data-stu-id="bb9cd-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="bb9cd-114">Instalando e removendo assemblies</span><span class="sxs-lookup"><span data-stu-id="bb9cd-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="bb9cd-115">Atualizando assemblies</span><span class="sxs-lookup"><span data-stu-id="bb9cd-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="bb9cd-116">Modos de reinstalação de assemblies do Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="bb9cd-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="bb9cd-117">Chaves do registro de assembly gravadas por Windows Installer</span><span class="sxs-lookup"><span data-stu-id="bb9cd-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="bb9cd-118">Para obter informações sobre como instalar aplicativos COM e COM+ 1,0, consulte [instalando um aplicativo com+ com o Windows Installer](installing-a-com--application-with-the-windows-installer.md), [instalando um componente com em um local privado](installing-a-com-component-to-a-private-location.md)e [tornar um componente com em um pacote existente privado](make-a-com-component-in-an-existing-package-private.md).</span><span class="sxs-lookup"><span data-stu-id="bb9cd-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
