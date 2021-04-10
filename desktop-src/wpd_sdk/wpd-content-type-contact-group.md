---
description: '\_grupo de \_ contatos de tipo de conteúdo WPD \_ \_'
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170984"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="172c9-103">\_grupo de \_ contatos de tipo de conteúdo WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="172c9-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="172c9-104">Um objeto que descreve seu tipo de tipo de conteúdo WPD- \_ \_ \_ \_ grupo de contatos representa um grupo de contatos.</span><span class="sxs-lookup"><span data-stu-id="172c9-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="172c9-105">As referências de objeto WPD deste objeto \_ \_ contêm uma lista de IDs de objeto para vários \_ objetos de contato de tipo de conteúdo WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="172c9-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="172c9-106">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="172c9-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="172c9-107">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="172c9-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="172c9-108">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="172c9-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="172c9-109">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="172c9-110">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="172c9-110">Required.</span></span>                                                             |
| [<span data-ttu-id="172c9-111">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="172c9-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="172c9-112">Required.</span></span>                                                             |
| [<span data-ttu-id="172c9-113">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="172c9-114">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="172c9-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="172c9-115">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="172c9-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="172c9-116">Required.</span></span>                                                             |
| [<span data-ttu-id="172c9-117">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="172c9-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="172c9-118">Required.</span></span>                                                             |
| [<span data-ttu-id="172c9-119">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="172c9-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="172c9-120">Required.</span></span>                                                             |
| [<span data-ttu-id="172c9-121">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="172c9-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="172c9-122">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="172c9-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="172c9-123">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="172c9-124">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="172c9-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="172c9-125">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="172c9-126">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="172c9-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="172c9-127">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="172c9-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="172c9-128">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="172c9-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="172c9-129">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="172c9-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="172c9-130">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="172c9-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="172c9-131">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="172c9-132">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="172c9-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="172c9-133">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="172c9-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="172c9-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="172c9-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="172c9-135">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="172c9-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="172c9-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="172c9-137">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="172c9-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="172c9-138">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="172c9-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="172c9-139">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="172c9-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="172c9-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="172c9-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="172c9-141">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="172c9-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="172c9-142">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="172c9-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="172c9-143">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="172c9-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="172c9-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="172c9-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="172c9-145">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="172c9-146">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="172c9-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="172c9-147">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="172c9-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="172c9-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="172c9-149">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="172c9-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="172c9-150">Opcional</span><span class="sxs-lookup"><span data-stu-id="172c9-150">Optional</span></span>                                                              |
| [<span data-ttu-id="172c9-151">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="172c9-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="172c9-152">Necessário se o objeto puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="172c9-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="172c9-153">\_localidade do \_ idioma do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="172c9-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="172c9-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="172c9-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="172c9-155">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="172c9-155">Typical Resources</span></span>

<span data-ttu-id="172c9-156">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="172c9-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="172c9-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="172c9-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="172c9-158">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="172c9-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



