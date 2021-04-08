---
description: Recupera informações para aplicativos que são importados.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Coleção FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089368"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="1526e-103">Coleção FilesForImport</span><span class="sxs-lookup"><span data-stu-id="1526e-103">FilesForImport collection</span></span>

<span data-ttu-id="1526e-104">Recupera informações para aplicativos que são importados.</span><span class="sxs-lookup"><span data-stu-id="1526e-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="1526e-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1526e-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1526e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1526e-106">Members</span></span>

<span data-ttu-id="1526e-107">A coleção **FilesForImport** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="1526e-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1526e-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="1526e-108">Related Collections</span></span>

<span data-ttu-id="1526e-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="1526e-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1526e-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1526e-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1526e-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1526e-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1526e-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="1526e-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="1526e-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="1526e-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1526e-114">**Básica**</span><span class="sxs-lookup"><span data-stu-id="1526e-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="1526e-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1526e-115">Properties</span></span>

<span data-ttu-id="1526e-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="1526e-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1526e-117">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="1526e-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="1526e-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1526e-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="1526e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="1526e-120">FileName</span><span class="sxs-lookup"><span data-stu-id="1526e-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="1526e-121">HasUsers</span><span class="sxs-lookup"><span data-stu-id="1526e-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="1526e-122">IsProxy</span><span class="sxs-lookup"><span data-stu-id="1526e-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="1526e-123">IsService</span><span class="sxs-lookup"><span data-stu-id="1526e-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="1526e-124">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="1526e-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="1526e-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="1526e-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="1526e-126">PartitionName</span><span class="sxs-lookup"><span data-stu-id="1526e-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="1526e-127">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="1526e-127">ApplicationFileName</span></span>



| <span data-ttu-id="1526e-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-128">Entry</span></span> | <span data-ttu-id="1526e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1526e-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-130">Description</span></span>    | <span data-ttu-id="1526e-131">O nome do arquivo MSI que contém o aplicativo que pode ser importado.</span><span class="sxs-lookup"><span data-stu-id="1526e-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="1526e-132">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-132">Access</span></span>         | <span data-ttu-id="1526e-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="1526e-134">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-134">Type</span></span>           | <span data-ttu-id="1526e-135">String</span><span class="sxs-lookup"><span data-stu-id="1526e-135">String</span></span>                                                                       |
| <span data-ttu-id="1526e-136">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-136">Default</span></span>        | <span data-ttu-id="1526e-137">N/D</span><span class="sxs-lookup"><span data-stu-id="1526e-137">N/A</span></span>                                                                          |
| <span data-ttu-id="1526e-138">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-138">Minimum system</span></span> | <span data-ttu-id="1526e-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="1526e-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1526e-140">ApplicationName</span></span>



| <span data-ttu-id="1526e-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-141">Entry</span></span> | <span data-ttu-id="1526e-142">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="1526e-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-143">Description</span></span>    | <span data-ttu-id="1526e-144">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1526e-144">The name of the application.</span></span> |
| <span data-ttu-id="1526e-145">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-145">Access</span></span>         | <span data-ttu-id="1526e-146">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-146">ReadOnly</span></span>                     |
| <span data-ttu-id="1526e-147">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-147">Type</span></span>           | <span data-ttu-id="1526e-148">String</span><span class="sxs-lookup"><span data-stu-id="1526e-148">String</span></span>                       |
| <span data-ttu-id="1526e-149">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-149">Default</span></span>        | <span data-ttu-id="1526e-150">""</span><span class="sxs-lookup"><span data-stu-id="1526e-150">""</span></span>                           |
| <span data-ttu-id="1526e-151">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-151">Minimum system</span></span> | <span data-ttu-id="1526e-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="1526e-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-153">Description</span></span>



| <span data-ttu-id="1526e-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-154">Entry</span></span> | <span data-ttu-id="1526e-155">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="1526e-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-156">Description</span></span>    | <span data-ttu-id="1526e-157">Uma descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1526e-157">A description of the application.</span></span> |
| <span data-ttu-id="1526e-158">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-158">Access</span></span>         | <span data-ttu-id="1526e-159">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-159">ReadOnly</span></span>                          |
| <span data-ttu-id="1526e-160">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-160">Type</span></span>           | <span data-ttu-id="1526e-161">String</span><span class="sxs-lookup"><span data-stu-id="1526e-161">String</span></span>                            |
| <span data-ttu-id="1526e-162">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-162">Default</span></span>        | <span data-ttu-id="1526e-163">""</span><span class="sxs-lookup"><span data-stu-id="1526e-163">""</span></span>                                |
| <span data-ttu-id="1526e-164">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-164">Minimum system</span></span> | <span data-ttu-id="1526e-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="1526e-166">FileName</span><span class="sxs-lookup"><span data-stu-id="1526e-166">FileName</span></span>



| <span data-ttu-id="1526e-167">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-167">Entry</span></span> | <span data-ttu-id="1526e-168">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1526e-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-169">Description</span></span>    | <span data-ttu-id="1526e-170">O nome do arquivo DLL ou EXE que contém o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1526e-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="1526e-171">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="1526e-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1526e-172">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-172">Access</span></span>         | <span data-ttu-id="1526e-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="1526e-174">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-174">Type</span></span>           | <span data-ttu-id="1526e-175">String</span><span class="sxs-lookup"><span data-stu-id="1526e-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="1526e-176">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-176">Default</span></span>        | <span data-ttu-id="1526e-177">""</span><span class="sxs-lookup"><span data-stu-id="1526e-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="1526e-178">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-178">Minimum system</span></span> | <span data-ttu-id="1526e-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="1526e-180">HasUsers</span><span class="sxs-lookup"><span data-stu-id="1526e-180">HasUsers</span></span>



| <span data-ttu-id="1526e-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-181">Entry</span></span> | <span data-ttu-id="1526e-182">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="1526e-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-183">Description</span></span>    | <span data-ttu-id="1526e-184">Indica se o aplicativo tem algum usuário.</span><span class="sxs-lookup"><span data-stu-id="1526e-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="1526e-185">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-185">Access</span></span>         | <span data-ttu-id="1526e-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="1526e-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="1526e-187">Type</span></span>           | <span data-ttu-id="1526e-188">Bool</span><span class="sxs-lookup"><span data-stu-id="1526e-188">Bool</span></span>                                             |
| <span data-ttu-id="1526e-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-189">Default</span></span>        | <span data-ttu-id="1526e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1526e-190">False</span></span>                                            |
| <span data-ttu-id="1526e-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-191">Minimum system</span></span> | <span data-ttu-id="1526e-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="1526e-193">IsProxy</span><span class="sxs-lookup"><span data-stu-id="1526e-193">IsProxy</span></span>



| <span data-ttu-id="1526e-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-194">Entry</span></span> | <span data-ttu-id="1526e-195">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="1526e-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-196">Description</span></span>    | <span data-ttu-id="1526e-197">Indica se o aplicativo é um proxy.</span><span class="sxs-lookup"><span data-stu-id="1526e-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="1526e-198">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-198">Access</span></span>         | <span data-ttu-id="1526e-199">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="1526e-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="1526e-200">Type</span></span>           | <span data-ttu-id="1526e-201">Bool</span><span class="sxs-lookup"><span data-stu-id="1526e-201">Bool</span></span>                                          |
| <span data-ttu-id="1526e-202">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-202">Default</span></span>        | <span data-ttu-id="1526e-203">Falso</span><span class="sxs-lookup"><span data-stu-id="1526e-203">False</span></span>                                         |
| <span data-ttu-id="1526e-204">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-204">Minimum system</span></span> | <span data-ttu-id="1526e-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="1526e-206">IsService</span><span class="sxs-lookup"><span data-stu-id="1526e-206">IsService</span></span>



| <span data-ttu-id="1526e-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-207">Entry</span></span> | <span data-ttu-id="1526e-208">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="1526e-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-209">Description</span></span>    | <span data-ttu-id="1526e-210">Indica se o aplicativo é um serviço.</span><span class="sxs-lookup"><span data-stu-id="1526e-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="1526e-211">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-211">Access</span></span>         | <span data-ttu-id="1526e-212">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="1526e-213">Tipo</span><span class="sxs-lookup"><span data-stu-id="1526e-213">Type</span></span>           | <span data-ttu-id="1526e-214">Bool</span><span class="sxs-lookup"><span data-stu-id="1526e-214">Bool</span></span>                                            |
| <span data-ttu-id="1526e-215">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-215">Default</span></span>        | <span data-ttu-id="1526e-216">Falso</span><span class="sxs-lookup"><span data-stu-id="1526e-216">False</span></span>                                           |
| <span data-ttu-id="1526e-217">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-217">Minimum system</span></span> | <span data-ttu-id="1526e-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1526e-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="1526e-219">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="1526e-219">PartitionDescription</span></span>



| <span data-ttu-id="1526e-220">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-220">Entry</span></span> | <span data-ttu-id="1526e-221">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="1526e-222">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-222">Description</span></span>    | <span data-ttu-id="1526e-223">Uma descrição da partição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1526e-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="1526e-224">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-224">Access</span></span>         | <span data-ttu-id="1526e-225">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="1526e-226">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-226">Type</span></span>           | <span data-ttu-id="1526e-227">String</span><span class="sxs-lookup"><span data-stu-id="1526e-227">String</span></span>                                        |
| <span data-ttu-id="1526e-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-228">Default</span></span>        | <span data-ttu-id="1526e-229">""</span><span class="sxs-lookup"><span data-stu-id="1526e-229">""</span></span>                                            |
| <span data-ttu-id="1526e-230">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-230">Minimum system</span></span> | <span data-ttu-id="1526e-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1526e-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="1526e-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="1526e-232">PartitionID</span></span>



| <span data-ttu-id="1526e-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-233">Entry</span></span> | <span data-ttu-id="1526e-234">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="1526e-235">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-235">Description</span></span>    | <span data-ttu-id="1526e-236">O GUID da partição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1526e-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="1526e-237">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-237">Access</span></span>         | <span data-ttu-id="1526e-238">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="1526e-239">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-239">Type</span></span>           | <span data-ttu-id="1526e-240">String</span><span class="sxs-lookup"><span data-stu-id="1526e-240">String</span></span>                                   |
| <span data-ttu-id="1526e-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-241">Default</span></span>        | <span data-ttu-id="1526e-242">""</span><span class="sxs-lookup"><span data-stu-id="1526e-242">""</span></span>                                       |
| <span data-ttu-id="1526e-243">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-243">Minimum system</span></span> | <span data-ttu-id="1526e-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1526e-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="1526e-245">PartitionName</span><span class="sxs-lookup"><span data-stu-id="1526e-245">PartitionName</span></span>



| <span data-ttu-id="1526e-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="1526e-246">Entry</span></span> | <span data-ttu-id="1526e-247">Valor</span><span class="sxs-lookup"><span data-stu-id="1526e-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="1526e-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="1526e-248">Description</span></span>    | <span data-ttu-id="1526e-249">O nome da partição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1526e-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="1526e-250">Access</span><span class="sxs-lookup"><span data-stu-id="1526e-250">Access</span></span>         | <span data-ttu-id="1526e-251">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1526e-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="1526e-252">Type</span><span class="sxs-lookup"><span data-stu-id="1526e-252">Type</span></span>           | <span data-ttu-id="1526e-253">String</span><span class="sxs-lookup"><span data-stu-id="1526e-253">String</span></span>                                   |
| <span data-ttu-id="1526e-254">Padrão</span><span class="sxs-lookup"><span data-stu-id="1526e-254">Default</span></span>        | <span data-ttu-id="1526e-255">""</span><span class="sxs-lookup"><span data-stu-id="1526e-255">""</span></span>                                       |
| <span data-ttu-id="1526e-256">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="1526e-256">Minimum system</span></span> | <span data-ttu-id="1526e-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1526e-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="1526e-258">Confira também</span><span class="sxs-lookup"><span data-stu-id="1526e-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1526e-259">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="1526e-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
