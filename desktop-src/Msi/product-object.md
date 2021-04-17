---
description: O objeto Product representa uma instância exclusiva de um produto que é anunciado, instalado ou desconhecido. O objeto pode ser instanciado com a Propriedade Product como &\# 0034; WindowsInstaller. Installer. Product (ProductCode, userid, contexto) &\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Objeto Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747953"
---
# <a name="product-object"></a><span data-ttu-id="e6525-103">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="e6525-103">Product object</span></span>

<span data-ttu-id="e6525-104">O objeto **Product** representa uma instância exclusiva de um produto que é anunciado, instalado ou desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e6525-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="e6525-105">O objeto pode ser instanciado com a propriedade **Product** como "WindowsInstaller. Installer. Product (*ProductCode*, *userid*, *Context*)".</span><span class="sxs-lookup"><span data-stu-id="e6525-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="e6525-106">*Userid* deve ser nulo para o contexto por máquina.</span><span class="sxs-lookup"><span data-stu-id="e6525-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="e6525-107">O *userid* pode ser nulo para o usuário atual especificado, quando o contexto não for por computador.</span><span class="sxs-lookup"><span data-stu-id="e6525-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="e6525-108">Os parâmetros de *ProductCode* e de *contexto* são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e6525-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="e6525-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e6525-109">Members</span></span>

<span data-ttu-id="e6525-110">O objeto **Product** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6525-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="e6525-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6525-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6525-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6525-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6525-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6525-113">Methods</span></span>

<span data-ttu-id="e6525-114">O objeto **Product** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e6525-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="e6525-115">Método</span><span class="sxs-lookup"><span data-stu-id="e6525-115">Method</span></span>                                                                 | <span data-ttu-id="e6525-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6525-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6525-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e6525-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="e6525-118">Adicione um disco ao conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="e6525-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="e6525-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="e6525-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="e6525-120">Adicione uma fonte de rede ou URL à lista de origem.</span><span class="sxs-lookup"><span data-stu-id="e6525-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="e6525-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="e6525-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="e6525-122">Limpa a lista de origem completa do tipo de fontes especificado.</span><span class="sxs-lookup"><span data-stu-id="e6525-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="e6525-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e6525-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="e6525-124">Remova um disco do conjunto de discos registrados da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="e6525-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="e6525-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="e6525-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="e6525-126">Remova uma rede ou origem da URL da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="e6525-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="e6525-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="e6525-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="e6525-128">Limpa a última fonte usada.</span><span class="sxs-lookup"><span data-stu-id="e6525-128">Clears the last used source.</span></span> <span data-ttu-id="e6525-129">Isso forçará uma resolução da lista de origem na próxima vez em que a origem for necessária.</span><span class="sxs-lookup"><span data-stu-id="e6525-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6525-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6525-130">Properties</span></span>

<span data-ttu-id="e6525-131">O objeto **Product** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6525-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="e6525-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e6525-132">Property</span></span>                                                      | <span data-ttu-id="e6525-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6525-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6525-134">**Componentestate**</span><span class="sxs-lookup"><span data-stu-id="e6525-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="e6525-135">O estado de um componente especificado para esta instância de produto.</span><span class="sxs-lookup"><span data-stu-id="e6525-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="e6525-136">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="e6525-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="e6525-137">Contexto desta instância de produto como um valor de MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="e6525-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="e6525-138">**Recurso**</span><span class="sxs-lookup"><span data-stu-id="e6525-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="e6525-139">O estado de um recurso especificado para esta instância do produto.</span><span class="sxs-lookup"><span data-stu-id="e6525-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="e6525-140">**Instalar a**</span><span class="sxs-lookup"><span data-stu-id="e6525-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="e6525-141">O valor de uma propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="e6525-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="e6525-142">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="e6525-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="e6525-143">Enumera todos os discos de mídia para esta instância de produto.</span><span class="sxs-lookup"><span data-stu-id="e6525-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="e6525-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="e6525-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="e6525-145">Retorna o código do produto.</span><span class="sxs-lookup"><span data-stu-id="e6525-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="e6525-146">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="e6525-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="e6525-147">Obter e definir as propriedades de informações de origem.</span><span class="sxs-lookup"><span data-stu-id="e6525-147">Get and set the source information properties.</span></span> <span data-ttu-id="e6525-148">Esta é uma propriedade de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e6525-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="e6525-149">**Fontes**</span><span class="sxs-lookup"><span data-stu-id="e6525-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="e6525-150">Enumera todas as fontes para esta instância do produto.</span><span class="sxs-lookup"><span data-stu-id="e6525-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="e6525-151">**Status**</span><span class="sxs-lookup"><span data-stu-id="e6525-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="e6525-152">Estado de instalação do produto.</span><span class="sxs-lookup"><span data-stu-id="e6525-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="e6525-153">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="e6525-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="e6525-154">Retorna o SID de usuário, sob a qual conta esta instância de produto está disponível.</span><span class="sxs-lookup"><span data-stu-id="e6525-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="e6525-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6525-155">Requirements</span></span>



| <span data-ttu-id="e6525-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6525-156">Requirement</span></span> | <span data-ttu-id="e6525-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e6525-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6525-158">Versão</span><span class="sxs-lookup"><span data-stu-id="e6525-158">Version</span></span><br/> | <span data-ttu-id="e6525-159">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6525-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6525-160">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6525-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6525-161">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e6525-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e6525-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e6525-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6525-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6525-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e6525-164">IID</span><span class="sxs-lookup"><span data-stu-id="e6525-164">IID</span></span><br/>     | <span data-ttu-id="e6525-165">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e6525-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="e6525-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6525-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6525-167">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e6525-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




