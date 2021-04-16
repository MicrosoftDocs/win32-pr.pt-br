---
description: O procedimento a seguir descreve como instalar assemblies lado a lado como assemblies compartilhados.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Instalando assemblies lado a lado como assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461040"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="be216-103">Instalando assemblies lado a lado como assemblies compartilhados</span><span class="sxs-lookup"><span data-stu-id="be216-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="be216-104">O procedimento a seguir descreve como instalar [assemblies lado a lado](about-side-by-side-assemblies-.md) como [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies).</span><span class="sxs-lookup"><span data-stu-id="be216-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="be216-105">**Para instalar um assembly lado a lado como um assembly compartilhado**</span><span class="sxs-lookup"><span data-stu-id="be216-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="be216-106">Assine e crie um catálogo para os arquivos no assembly.</span><span class="sxs-lookup"><span data-stu-id="be216-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="be216-107">Os arquivos devem ser assinados para instalá-los como assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="be216-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="be216-108">Para obter mais informações, consulte [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="be216-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="be216-109">Você deve instalar assemblies compartilhados lado a lado como componentes de um pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="be216-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="be216-110">Esse pode ser o mesmo pacote de instalação usado para instalar ou atualizar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be216-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="be216-111">Se o assembly compartilhado for enviado como parte de vários aplicativos, você deverá fornecer um módulo de mesclagem que possa ser incorporado nos pacotes de instalação desses aplicativos e criar um catálogo para os arquivos no assembly.</span><span class="sxs-lookup"><span data-stu-id="be216-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="be216-112">Windows Installer versão 2,0 ou posterior é necessária para instalar assemblies.</span><span class="sxs-lookup"><span data-stu-id="be216-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="be216-113">Para obter mais informações, consulte o SDK do [Windows Installer](../msi/windows-installer-portal.md) e as seções em [instalação de assemblies do Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="be216-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
