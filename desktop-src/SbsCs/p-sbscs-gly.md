---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (aplicativos isolados e assemblies lado a lado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370570"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="8c5be-103">P (aplicativos isolados e assemblies lado a lado)</span><span class="sxs-lookup"><span data-stu-id="8c5be-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="8c5be-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="8c5be-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8c5be-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configuração por aplicativo**</span><span class="sxs-lookup"><span data-stu-id="8c5be-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="8c5be-106">Configuração que pode substituir a configuração de aplicativo global de um assembly específico.</span><span class="sxs-lookup"><span data-stu-id="8c5be-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="8c5be-107">Uma configuração por aplicativo é especificada por um arquivo de manifesto de configuração de aplicativo instalado na mesma pasta que o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="8c5be-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="8c5be-108">O arquivo de manifesto descreve a versão, ou o intervalo de versões, de assemblies lado a lado a serem usados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c5be-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="8c5be-109">A configuração por aplicativo pode ser usada quando uma nova versão de um assembly é incompatível com um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c5be-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="8c5be-110">Nesse caso, a configuração padrão ou global do aplicativo pode ser substituída por um assembly lado a lado específico.</span><span class="sxs-lookup"><span data-stu-id="8c5be-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="8c5be-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly lado a lado privado**</span><span class="sxs-lookup"><span data-stu-id="8c5be-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="8c5be-112">Um assembly lado a lado privado só é visível para um aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="8c5be-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="8c5be-113">Ele é instalado localmente em um aplicativo isolado e o código do assembly se torna privado para o contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c5be-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="8c5be-114">As dependências de um assembly lado a lado privado são descritas no arquivo de manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c5be-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="8c5be-115">Assemblies privados lado a lado podem ser usados para deslocar os efeitos negativos do compartilhamento de assembly, como conflitos de DLL e para facilitar a implantação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c5be-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="8c5be-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8c5be-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="8c5be-117">Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o assembly está assinado.</span><span class="sxs-lookup"><span data-stu-id="8c5be-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="8c5be-118">A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais.</span><span class="sxs-lookup"><span data-stu-id="8c5be-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="8c5be-119">Necessário para todos os assemblies compartilhados lado a lado.</span><span class="sxs-lookup"><span data-stu-id="8c5be-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 



