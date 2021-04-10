---
description: Um assembly Win32 pode ser instalado como um assembly privado e estar exclusivamente disponível para uso por um aplicativo. Os assemblies privados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assemblies particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169844"
---
# <a name="private-assemblies"></a><span data-ttu-id="bf66b-104">Assemblies particulares</span><span class="sxs-lookup"><span data-stu-id="bf66b-104">Private Assemblies</span></span>

<span data-ttu-id="bf66b-105">Um assembly Win32 pode ser instalado como um assembly privado e estar exclusivamente disponível para uso por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf66b-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="bf66b-106">Os assemblies privados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf66b-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="bf66b-107">No Windows XP, os assemblies privados são instalados como [assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="bf66b-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="bf66b-108">O Windows Installer instala assemblies privados lado a lado em uma pasta privada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf66b-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="bf66b-109">Normalmente, a pasta que contém o arquivo executável dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bf66b-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="bf66b-110">A dependência do aplicativo no assembly particular é especificada em um arquivo de manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf66b-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="bf66b-111">Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="bf66b-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="bf66b-112">Em sistemas operacionais anteriores ao Windows XP, uma cópia do assembly particular e um arquivo. local são instalados em uma pasta particular para o uso exclusivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf66b-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="bf66b-113">Uma versão do assembly também é registrada globalmente no sistema e disponível para qualquer aplicativo que se vincule a ele.</span><span class="sxs-lookup"><span data-stu-id="bf66b-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="bf66b-114">A versão global do assembly pode ser a versão instalada com o aplicativo ou uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="bf66b-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="bf66b-115">A versão global é determinada pelas mesmas regras usadas por [componentes isolados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="bf66b-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="bf66b-116">Observe que o Windows Installer não pode instalar um assembly privado em um local que tenha um caminho que contenha mais de 234 caracteres, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="bf66b-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
