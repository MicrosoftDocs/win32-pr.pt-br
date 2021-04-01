---
description: '\_tipo de conteúdo WPD \_ \_ não especificado'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b767ba2d76dc569def42b80eb646ae0e6a6aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829586"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="1f8c6-103">\_tipo de conteúdo WPD \_ \_ não especificado</span><span class="sxs-lookup"><span data-stu-id="1f8c6-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="1f8c6-104">Um objeto que descreve seu tipo como \_ tipo de conteúdo WPD \_ \_ não especificado representa um objeto genérico que pode ou não ter um arquivo físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="1f8c6-105">A diferença entre este tipo e o \_ arquivo genérico do tipo de conteúdo WPD \_ \_ \_ é que os \_ objetos de arquivo genéricos do tipo de conteúdo WPD \_ \_ \_ devem ter um arquivo físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="1f8c6-106">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-106">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="1f8c6-107">**Nome da propriedade**</span><span class="sxs-lookup"><span data-stu-id="1f8c6-107">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="1f8c6-108">**Obrigatório ou opcional**</span><span class="sxs-lookup"><span data-stu-id="1f8c6-108">**Required or Optional**</span></span>                                                      |
| [<span data-ttu-id="1f8c6-109">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="1f8c6-110">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-110">Required, read-only.</span></span> <span data-ttu-id="1f8c6-111">Um cliente não pode definir essa propriedade mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="1f8c6-112">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="1f8c6-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-114">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="1f8c6-115">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="1f8c6-116">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="1f8c6-117">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-117">Required, read-only.</span></span> <span data-ttu-id="1f8c6-118">Um cliente não pode definir essa propriedade mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="1f8c6-119">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="1f8c6-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-121">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="1f8c6-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-123">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="1f8c6-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="1f8c6-124">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="1f8c6-125">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="1f8c6-126">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="1f8c6-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="1f8c6-127">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="1f8c6-128">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="1f8c6-129">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="1f8c6-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="1f8c6-130">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="1f8c6-131">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="1f8c6-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="1f8c6-132">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="1f8c6-133">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="1f8c6-134">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="1f8c6-135">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="1f8c6-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="1f8c6-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-137">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="1f8c6-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-139">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="1f8c6-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="1f8c6-140">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="1f8c6-141">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="1f8c6-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="1f8c6-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-143">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="1f8c6-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="1f8c6-144">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="1f8c6-145">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="1f8c6-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="1f8c6-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-147">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="1f8c6-148">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="1f8c6-149">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="1f8c6-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-151">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="1f8c6-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="1f8c6-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="1f8c6-153">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="1f8c6-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="1f8c6-154">Obrigatório se o objeto não puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="1f8c6-155">\_localidade do \_ idioma do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f8c6-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="1f8c6-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="1f8c6-157">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="1f8c6-157">Typical Resources</span></span>

<span data-ttu-id="1f8c6-158">Esses objetos normalmente incluem os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="1f8c6-159">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="1f8c6-159">Resource Name</span></span>                                          | <span data-ttu-id="1f8c6-160">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="1f8c6-160">Required or Optional</span></span>                             | <span data-ttu-id="1f8c6-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f8c6-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="1f8c6-162">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1f8c6-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="1f8c6-163">Necessário se o objeto for apoiado por dados binários.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="1f8c6-164">Contém os dados binários.</span><span class="sxs-lookup"><span data-stu-id="1f8c6-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1f8c6-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f8c6-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8c6-166">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="1f8c6-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



