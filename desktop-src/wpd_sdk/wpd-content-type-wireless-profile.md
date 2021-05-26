---
description: '\_ \_ \_ perfil sem fio do tipo de conteúdo WPD \_'
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423696"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="a8e78-103">\_ \_ \_ perfil sem fio do tipo de conteúdo WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="a8e78-104">Um objeto que descreve seu tipo de \_ \_ perfil sem fio do tipo de conteúdo WPD \_ \_ representa informações usadas para acessar uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="a8e78-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="a8e78-105">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8e78-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="a8e78-106">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="a8e78-106">Property Name</span></span>             | <span data-ttu-id="a8e78-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="a8e78-107">Required or Optional</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="a8e78-108">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="a8e78-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a8e78-109">Required.</span></span>                                                             |
| [<span data-ttu-id="a8e78-110">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="a8e78-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a8e78-111">Required.</span></span>                                                             |
| [<span data-ttu-id="a8e78-112">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="a8e78-113">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a8e78-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="a8e78-114">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="a8e78-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a8e78-115">Required.</span></span>                                                             |
| [<span data-ttu-id="a8e78-116">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="a8e78-117">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a8e78-117">Required.</span></span>                                                             |
| [<span data-ttu-id="a8e78-118">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="a8e78-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a8e78-119">Required.</span></span>                                                             |
| [<span data-ttu-id="a8e78-120">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="a8e78-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="a8e78-121">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="a8e78-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="a8e78-122">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="a8e78-123">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="a8e78-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="a8e78-124">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="a8e78-125">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="a8e78-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="a8e78-126">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a8e78-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="a8e78-127">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a8e78-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="a8e78-128">OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL</span><span class="sxs-lookup"><span data-stu-id="a8e78-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="a8e78-129">Recomendado se o objeto não for destinado ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8e78-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="a8e78-130">REFERÊNCIAS DE OBJETO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="a8e78-131">Necessário se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="a8e78-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="a8e78-132">PALAVRAS-CHAVE \_ DE OBJETO WPD \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="a8e78-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="a8e78-134">ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a8e78-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="a8e78-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="a8e78-136">O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_</span><span class="sxs-lookup"><span data-stu-id="a8e78-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="a8e78-137">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="a8e78-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="a8e78-138">DATA DO OBJETO WPD \_ \_ \_ CRIADO</span><span class="sxs-lookup"><span data-stu-id="a8e78-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="a8e78-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="a8e78-140">WPD \_ OBJECT \_ DATE \_ MODIFIED</span><span class="sxs-lookup"><span data-stu-id="a8e78-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="a8e78-141">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="a8e78-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="a8e78-142">WPD \_ OBJECT \_ DATE \_ AUTHORED</span><span class="sxs-lookup"><span data-stu-id="a8e78-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="a8e78-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="a8e78-144">REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD</span><span class="sxs-lookup"><span data-stu-id="a8e78-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="a8e78-145">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="a8e78-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="a8e78-146">ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a8e78-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="a8e78-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="a8e78-148">OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO</span><span class="sxs-lookup"><span data-stu-id="a8e78-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="a8e78-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="a8e78-150">O OBJETO WPD \_ \_ PODE \_ EXCLUIR</span><span class="sxs-lookup"><span data-stu-id="a8e78-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="a8e78-151">Necessário se o objeto não puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="a8e78-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="a8e78-152">LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a8e78-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="a8e78-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e78-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="a8e78-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="a8e78-154">Typical Resources</span></span>

<span data-ttu-id="a8e78-155">Esses objetos normalmente incluem os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="a8e78-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="a8e78-156">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="a8e78-156">Resource Name</span></span>                                          | <span data-ttu-id="a8e78-157">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="a8e78-157">Required or Optional</span></span>                                  | <span data-ttu-id="a8e78-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8e78-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="a8e78-159">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a8e78-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="a8e78-160">Necessário se o objeto for representado por dados binários.</span><span class="sxs-lookup"><span data-stu-id="a8e78-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="a8e78-161">Contém os dados binários.</span><span class="sxs-lookup"><span data-stu-id="a8e78-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a8e78-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8e78-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8e78-163">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="a8e78-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



