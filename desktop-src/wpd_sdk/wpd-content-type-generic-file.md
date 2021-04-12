---
description: '\_ \_ mensagem genérica do tipo de conteúdo WPD \_ \_'
ms.assetid: 8e58d15f-ee51-42c2-9d8b-6c3b9c730ff4
title: WPD_CONTENT_TYPE_GENERIC_MESSAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febde68787366dc0f84b1b187f1393017ceb9c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297128"
---
# <a name="wpd_content_type_generic_message"></a><span data-ttu-id="09182-103">\_ \_ mensagem genérica do tipo de conteúdo WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="09182-103">WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE</span></span>

<span data-ttu-id="09182-104">Um objeto que descreve seu tipo de \_ \_ mensagem genérica tipo de conteúdo WPD \_ \_ representa uma mensagem, por exemplo, SMS, email e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="09182-104">An object that describes its type as WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE represents a message, for example, SMS, e-mail, and so on.</span></span>

<span data-ttu-id="09182-105">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="09182-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="09182-106">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="09182-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="09182-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="09182-107">Required or Optional</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="09182-108">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="09182-109">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09182-109">Required, read-only.</span></span> <span data-ttu-id="09182-110">Um cliente não pode definir essa propriedade, mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="09182-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="09182-111">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="09182-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="09182-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="09182-113">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="09182-114">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="09182-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="09182-115">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="09182-116">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09182-116">Required, read-only.</span></span> <span data-ttu-id="09182-117">Um cliente não pode definir essa propriedade, mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="09182-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="09182-118">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="09182-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="09182-119">Required.</span></span>                                                                      |
| [<span data-ttu-id="09182-120">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="09182-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="09182-121">Required.</span></span>                                                                      |
| [<span data-ttu-id="09182-122">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="09182-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="09182-123">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="09182-123">Required if the object is hidden.</span></span>                                              |
| [<span data-ttu-id="09182-124">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="09182-125">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="09182-125">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="09182-126">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="09182-127">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="09182-127">Required if the object has at least one resource.</span></span>                              |
| [<span data-ttu-id="09182-128">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="09182-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="09182-129">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="09182-129">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="09182-130">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="09182-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="09182-131">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09182-131">Recommended if the object is not meant for consumption by the device.</span></span>          |
| [<span data-ttu-id="09182-132">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="09182-133">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="09182-133">Required if the object has references to other objects.</span></span>                        |
| [<span data-ttu-id="09182-134">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="09182-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="09182-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-135">Optional.</span></span>                                                                      |
| [<span data-ttu-id="09182-136">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="09182-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-137">Optional.</span></span>                                                                      |
| [<span data-ttu-id="09182-138">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="09182-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="09182-139">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="09182-139">Required if the object is protected by DRM technology.</span></span>                         |
| [<span data-ttu-id="09182-140">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="09182-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="09182-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-141">Optional.</span></span>                                                                      |
| [<span data-ttu-id="09182-142">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="09182-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="09182-143">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="09182-143">Recommended.</span></span>                                                                   |
| [<span data-ttu-id="09182-144">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="09182-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="09182-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-145">Optional.</span></span>                                                                      |
| [<span data-ttu-id="09182-146">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="09182-147">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="09182-147">Recommended if the object is referenced by another object.</span></span>                     |
| [<span data-ttu-id="09182-148">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="09182-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-149">Optional.</span></span>                                                                      |
| [<span data-ttu-id="09182-150">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="09182-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="09182-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-151">Optional.</span></span>                                                                      |
| [<span data-ttu-id="09182-152">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="09182-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="09182-153">Necessário se o objeto puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="09182-153">Required if the object can be deleted.</span></span>                                         |
| [<span data-ttu-id="09182-154">\_localidade do \_ idioma do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="09182-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="09182-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09182-155">Optional.</span></span>                                                                      |



 

## <a name="typical-resources"></a><span data-ttu-id="09182-156">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="09182-156">Typical Resources</span></span>

<span data-ttu-id="09182-157">Esses objetos normalmente incluem os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="09182-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="09182-158">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="09182-158">Resource Name</span></span>                                          | <span data-ttu-id="09182-159">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="09182-159">Required or Optional</span></span>                                  | <span data-ttu-id="09182-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="09182-160">Description</span></span>        |
|--------------------------------------------------------|-------------------------------------------------------|--------------------|
| [<span data-ttu-id="09182-161">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="09182-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="09182-162">Necessário se o objeto tiver suporte com dados binários.</span><span class="sxs-lookup"><span data-stu-id="09182-162">Required if the object is supported with binary data.</span></span> | <span data-ttu-id="09182-163">Contém os dados.</span><span class="sxs-lookup"><span data-stu-id="09182-163">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09182-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09182-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09182-165">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="09182-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



