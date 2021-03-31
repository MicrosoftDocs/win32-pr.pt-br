---
title: Determinando a versão do BITS em um computador
description: Para determinar a versão do BITS no computador cliente, verifique a versão do QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635022"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="f7c42-103">Determinando a versão do BITS em um computador</span><span class="sxs-lookup"><span data-stu-id="f7c42-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="f7c42-104">Para determinar a versão do BITS no computador cliente, verifique a versão do QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="f7c42-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="f7c42-105">Para localizar o número de versão da DLL:</span><span class="sxs-lookup"><span data-stu-id="f7c42-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="f7c42-106">Localize QMgr.dll em% windir% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="f7c42-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="f7c42-107">Clique com o botão direito do mouse em QMgr.dll e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f7c42-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="f7c42-108">Clique na guia **versão** .</span><span class="sxs-lookup"><span data-stu-id="f7c42-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="f7c42-109">Observe o número de versão.</span><span class="sxs-lookup"><span data-stu-id="f7c42-109">Note the version number.</span></span>

<span data-ttu-id="f7c42-110">Você também pode usar o seguinte código do PowerShell para determinar a versão do. dll no seu sistema:</span><span class="sxs-lookup"><span data-stu-id="f7c42-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="f7c42-111">Se a DLL também existir em% windir% \\ System32 \\ bits, repita as etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="f7c42-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="f7c42-112">O BITS usa a DLL com o número de versão mais alto.</span><span class="sxs-lookup"><span data-stu-id="f7c42-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="f7c42-113">A tabela a seguir lista as versões do BITS e seus números de versão de arquivo QMgr.dll correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f7c42-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="f7c42-114">Versão do BITS</span><span class="sxs-lookup"><span data-stu-id="f7c42-114">BITS version</span></span> | <span data-ttu-id="f7c42-115">Número de versão do arquivo QMgr.dll</span><span class="sxs-lookup"><span data-stu-id="f7c42-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="f7c42-116">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="f7c42-116">BITS 10.1</span></span>    | <span data-ttu-id="f7c42-117">7.8. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-118">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-118">BITS 5.0</span></span>     | <span data-ttu-id="f7c42-119">7.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-120">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-120">BITS 4.0</span></span>     | <span data-ttu-id="f7c42-121">7.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-122">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-122">BITS 3.0</span></span>     | <span data-ttu-id="f7c42-123">7.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-124">BITS 2,5</span><span class="sxs-lookup"><span data-stu-id="f7c42-124">BITS 2.5</span></span>     | <span data-ttu-id="f7c42-125">6.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-126">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-126">BITS 2.0</span></span>     | <span data-ttu-id="f7c42-127">6.6. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-128">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="f7c42-128">BITS 1.5</span></span>     | <span data-ttu-id="f7c42-129">6.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-130">BITS 1,2</span><span class="sxs-lookup"><span data-stu-id="f7c42-130">BITS 1.2</span></span>     | <span data-ttu-id="f7c42-131">6.2. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="f7c42-132">BITS 1,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-132">BITS 1.0</span></span>     | <span data-ttu-id="f7c42-133">6.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="f7c42-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="f7c42-134">Você também pode usar os identificadores de classe simbólicos para determinar a versão do BITS que está registrada no computador.</span><span class="sxs-lookup"><span data-stu-id="f7c42-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="f7c42-135">A tabela a seguir lista as versões do BITS e seus identificadores de classe simbólico correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f7c42-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="f7c42-136">A função **CoCreateInstance** retornará **REGDB \_ E \_ CLASSNOTREG** se a classe não estiver registrada.</span><span class="sxs-lookup"><span data-stu-id="f7c42-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="f7c42-137">Versão do BITS</span><span class="sxs-lookup"><span data-stu-id="f7c42-137">BITS version</span></span>  | <span data-ttu-id="f7c42-138">Identificador de classe simbólico</span><span class="sxs-lookup"><span data-stu-id="f7c42-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="f7c42-139">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="f7c42-139">BITS 10.1</span></span>     | <span data-ttu-id="f7c42-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f7c42-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="f7c42-141">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-141">BITS 5.0</span></span>      | <span data-ttu-id="f7c42-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7c42-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="f7c42-143">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-143">BITS 4.0</span></span>      | <span data-ttu-id="f7c42-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7c42-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="f7c42-145">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-145">BITS 3.0</span></span>      | <span data-ttu-id="f7c42-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7c42-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="f7c42-147">BITS 2,5</span><span class="sxs-lookup"><span data-stu-id="f7c42-147">BITS 2.5</span></span>      | <span data-ttu-id="f7c42-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="f7c42-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="f7c42-149">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-149">BITS 2.0</span></span>      | <span data-ttu-id="f7c42-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7c42-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="f7c42-151">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="f7c42-151">BITS 1.5</span></span>      | <span data-ttu-id="f7c42-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="f7c42-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="f7c42-153">BITS 1,2, 1,0</span><span class="sxs-lookup"><span data-stu-id="f7c42-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="f7c42-154">\_BACKGROUNDCOPYMANAGER CLSID</span><span class="sxs-lookup"><span data-stu-id="f7c42-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




