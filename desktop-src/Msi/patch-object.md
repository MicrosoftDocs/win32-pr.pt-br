---
description: O objeto patch representa uma instância exclusiva de um patch que foi registrado ou aplicado. O objeto pode ser instanciado com a propriedade patch como &\# 0034; WindowsInstaller. Installer. patch (PatchCode, ProductCode, userid, contexto) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Objeto patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751641"
---
# <a name="patch-object"></a><span data-ttu-id="44ead-103">Objeto patch</span><span class="sxs-lookup"><span data-stu-id="44ead-103">Patch object</span></span>

<span data-ttu-id="44ead-104">O objeto **patch** representa uma instância exclusiva de um patch que foi registrado ou aplicado.</span><span class="sxs-lookup"><span data-stu-id="44ead-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="44ead-105">O objeto pode ser instanciado com a propriedade **patch** como "WindowsInstaller. Installer. patch (*PatchCode*, *ProductCode*, *userid*, *Context*)".</span><span class="sxs-lookup"><span data-stu-id="44ead-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="44ead-106">Para um contexto de computador, o parâmetro *userid* deve ser uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="44ead-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="44ead-107">O *ProductCode* pode ser definido como uma cadeia de caracteres vazia para patches que são registrados apenas e que ainda não foram aplicados a nenhum produto.</span><span class="sxs-lookup"><span data-stu-id="44ead-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="44ead-108">O *ProductCode* pode ser definido como uma cadeia de caracteres vazia ao ler ou atualizar informações da lista de origem de um patch.</span><span class="sxs-lookup"><span data-stu-id="44ead-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="44ead-109">Membros</span><span class="sxs-lookup"><span data-stu-id="44ead-109">Members</span></span>

<span data-ttu-id="44ead-110">O objeto **patch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="44ead-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="44ead-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="44ead-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="44ead-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44ead-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="44ead-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="44ead-113">Methods</span></span>

<span data-ttu-id="44ead-114">O objeto **patch** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="44ead-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="44ead-115">Método</span><span class="sxs-lookup"><span data-stu-id="44ead-115">Method</span></span>                                                               | <span data-ttu-id="44ead-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="44ead-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ead-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="44ead-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="44ead-118">Adicione um disco ao conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="44ead-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="44ead-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="44ead-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="44ead-120">Adicione uma fonte de rede ou URL à lista de origem.</span><span class="sxs-lookup"><span data-stu-id="44ead-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="44ead-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="44ead-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="44ead-122">Limpa a lista de origem completa do tipo de fontes especificado.</span><span class="sxs-lookup"><span data-stu-id="44ead-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="44ead-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="44ead-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="44ead-124">Remova um disco do conjunto de discos registrados da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="44ead-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="44ead-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="44ead-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="44ead-126">Remova uma rede ou origem da URL da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="44ead-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="44ead-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="44ead-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="44ead-128">Limpa a última fonte usada da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="44ead-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="44ead-129">Isso forçará uma resolução da lista de origem na próxima vez em que a origem for necessária.</span><span class="sxs-lookup"><span data-stu-id="44ead-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="44ead-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44ead-130">Properties</span></span>

<span data-ttu-id="44ead-131">O objeto **patch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="44ead-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="44ead-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="44ead-132">Property</span></span>                                                  | <span data-ttu-id="44ead-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="44ead-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ead-134">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="44ead-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="44ead-135">O contexto dessa instância de patch é um valor de MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="44ead-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="44ead-136">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="44ead-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="44ead-137">Enumera todos os discos de mídia para esta instância de patch.</span><span class="sxs-lookup"><span data-stu-id="44ead-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="44ead-138">**PatchCode**</span><span class="sxs-lookup"><span data-stu-id="44ead-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="44ead-139">Retorna o código do patch.</span><span class="sxs-lookup"><span data-stu-id="44ead-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="44ead-140">**Patchproperty**</span><span class="sxs-lookup"><span data-stu-id="44ead-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="44ead-141">Obtém informações de propriedade sobre um patch específico aplicado a uma instância específica do produto.</span><span class="sxs-lookup"><span data-stu-id="44ead-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="44ead-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="44ead-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="44ead-143">Retorna o código do produto.</span><span class="sxs-lookup"><span data-stu-id="44ead-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="44ead-144">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="44ead-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="44ead-145">Obtém e define as propriedades de informações de origem.</span><span class="sxs-lookup"><span data-stu-id="44ead-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="44ead-146">Esta é uma propriedade de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="44ead-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="44ead-147">**Fontes**</span><span class="sxs-lookup"><span data-stu-id="44ead-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="44ead-148">Enumera todas as fontes para esta instância de patch.</span><span class="sxs-lookup"><span data-stu-id="44ead-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="44ead-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="44ead-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="44ead-150">Estado da instalação do patch.</span><span class="sxs-lookup"><span data-stu-id="44ead-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="44ead-151">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="44ead-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="44ead-152">Retorna o SID do usuário, na conta em que esta instância de patch está disponível.</span><span class="sxs-lookup"><span data-stu-id="44ead-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="44ead-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ead-153">Requirements</span></span>



| <span data-ttu-id="44ead-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ead-154">Requirement</span></span> | <span data-ttu-id="44ead-155">Valor</span><span class="sxs-lookup"><span data-stu-id="44ead-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44ead-156">Versão</span><span class="sxs-lookup"><span data-stu-id="44ead-156">Version</span></span><br/> | <span data-ttu-id="44ead-157">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44ead-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="44ead-158">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44ead-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="44ead-159">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="44ead-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="44ead-160">DLL</span><span class="sxs-lookup"><span data-stu-id="44ead-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="44ead-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ead-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="44ead-162">IID</span><span class="sxs-lookup"><span data-stu-id="44ead-162">IID</span></span><br/>     | <span data-ttu-id="44ead-163">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="44ead-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="44ead-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="44ead-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ead-165">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="44ead-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




