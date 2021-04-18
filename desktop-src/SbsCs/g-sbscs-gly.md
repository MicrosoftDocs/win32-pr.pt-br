---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: G (aplicativos isolados e assemblies lado a lado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747933"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="72f1d-103">G (aplicativos isolados e assemblies lado a lado)</span><span class="sxs-lookup"><span data-stu-id="72f1d-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="72f1d-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="72f1d-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="72f1d-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**configuração de aplicativo global**</span><span class="sxs-lookup"><span data-stu-id="72f1d-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="72f1d-106">Especificação que todos os aplicativos no sistema usam a mesma versão do assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="72f1d-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="72f1d-107">A configuração global é especificada em uma base por assembly em um arquivo de manifesto de assembly global instalado na pasta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="72f1d-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="72f1d-108">A configuração global pode ser usada quando um desenvolvedor ou administrador de assembly precisar configurar todos os aplicativos no sistema para usar uma versão de assembly mais recente.</span><span class="sxs-lookup"><span data-stu-id="72f1d-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="72f1d-109">Nesse caso, o novo assembly precisa ser compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="72f1d-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="72f1d-110">Uma configuração por aplicativo substitui a configuração de aplicativo padrão ou global para aplicativos específicos.</span><span class="sxs-lookup"><span data-stu-id="72f1d-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="72f1d-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**manifesto de assembly global**</span><span class="sxs-lookup"><span data-stu-id="72f1d-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="72f1d-112">Arquivo que define a configuração de aplicativo global de um assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="72f1d-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="72f1d-113">Os arquivos de manifesto de assembly global são instalados no repositório de assemblies do sistema na pasta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="72f1d-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



