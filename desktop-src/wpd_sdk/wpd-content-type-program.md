---
description: '\_programa de \_ tipo de conteúdo WPD \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0187d4e87f47e8210e94a676ca9ccd1e1364cf1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662801"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="c607d-103">\_programa de \_ tipo de conteúdo WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="c607d-104">Um objeto que descreve seu tipo de \_ programa de tipo de conteúdo WPD \_ \_ representa um programa executável.</span><span class="sxs-lookup"><span data-stu-id="c607d-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="c607d-105">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c607d-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c607d-106">**Nome da propriedade**</span><span class="sxs-lookup"><span data-stu-id="c607d-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="c607d-107">**Obrigatório ou opcional**</span><span class="sxs-lookup"><span data-stu-id="c607d-107">**Required or Optional**</span></span>                                                           |
| [<span data-ttu-id="c607d-108">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="c607d-109">Obrigatório, mas somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c607d-109">Required, but read-only.</span></span> <span data-ttu-id="c607d-110">Um cliente não pode definir essa propriedade, mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="c607d-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="c607d-111">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="c607d-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c607d-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="c607d-113">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="c607d-114">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c607d-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="c607d-115">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="c607d-116">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c607d-116">Required, read-only.</span></span> <span data-ttu-id="c607d-117">Um cliente não pode definir essa propriedade mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="c607d-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="c607d-118">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="c607d-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c607d-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="c607d-120">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="c607d-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c607d-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="c607d-122">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="c607d-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="c607d-123">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="c607d-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="c607d-124">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="c607d-125">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="c607d-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="c607d-126">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="c607d-127">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="c607d-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="c607d-128">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c607d-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="c607d-129">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c607d-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="c607d-130">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="c607d-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="c607d-131">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c607d-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="c607d-132">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="c607d-133">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="c607d-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="c607d-134">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="c607d-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="c607d-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="c607d-136">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="c607d-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="c607d-138">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="c607d-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="c607d-139">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="c607d-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="c607d-140">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="c607d-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="c607d-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="c607d-142">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="c607d-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="c607d-143">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="c607d-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="c607d-144">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="c607d-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="c607d-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="c607d-146">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="c607d-147">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="c607d-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="c607d-148">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="c607d-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="c607d-150">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="c607d-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="c607d-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="c607d-152">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="c607d-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="c607d-153">Obrigatório se o objeto não puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c607d-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="c607d-154">\_localidade do \_ idioma do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c607d-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="c607d-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c607d-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="c607d-156">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="c607d-156">Typical Resources</span></span>

<span data-ttu-id="c607d-157">Esses objetos normalmente incluem os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="c607d-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="c607d-158">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="c607d-158">Resource Name</span></span>                                          | <span data-ttu-id="c607d-159">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="c607d-159">Required or Optional</span></span> | <span data-ttu-id="c607d-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="c607d-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="c607d-161">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c607d-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="c607d-162">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c607d-162">Required.</span></span>            | <span data-ttu-id="c607d-163">Contém o arquivo de programa.</span><span class="sxs-lookup"><span data-stu-id="c607d-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c607d-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c607d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c607d-165">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="c607d-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



