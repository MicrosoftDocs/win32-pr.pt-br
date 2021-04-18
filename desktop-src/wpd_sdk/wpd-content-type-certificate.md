---
description: '\_certificado de \_ tipo de conteúdo WPD \_'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786230"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="29921-103">\_certificado de \_ tipo de conteúdo WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="29921-104">Um objeto que descreve seu tipo de \_ certificado de tipo de conteúdo WPD \_ \_ representa um certificado usado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="29921-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="29921-105">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="29921-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="29921-106">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="29921-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="29921-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="29921-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="29921-108">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="29921-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29921-109">Required.</span></span>                                                             |
| [<span data-ttu-id="29921-110">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="29921-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29921-111">Required.</span></span>                                                             |
| [<span data-ttu-id="29921-112">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="29921-113">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="29921-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="29921-114">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="29921-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29921-115">Required.</span></span>                                                             |
| [<span data-ttu-id="29921-116">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="29921-117">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29921-117">Required.</span></span>                                                             |
| [<span data-ttu-id="29921-118">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="29921-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29921-119">Required.</span></span>                                                             |
| [<span data-ttu-id="29921-120">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="29921-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="29921-121">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="29921-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="29921-122">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="29921-123">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="29921-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="29921-124">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="29921-125">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="29921-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="29921-126">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="29921-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="29921-127">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="29921-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="29921-128">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="29921-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="29921-129">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29921-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="29921-130">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="29921-131">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="29921-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="29921-132">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="29921-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="29921-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="29921-134">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="29921-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="29921-136">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="29921-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="29921-137">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="29921-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="29921-138">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="29921-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="29921-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="29921-140">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="29921-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="29921-141">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="29921-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="29921-142">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="29921-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="29921-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="29921-144">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="29921-145">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="29921-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="29921-146">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="29921-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="29921-148">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="29921-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="29921-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="29921-150">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="29921-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="29921-151">Necessário se o objeto puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="29921-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="29921-152">\_localidade do \_ idioma do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="29921-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="29921-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29921-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="29921-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="29921-154">Typical Resources</span></span>

<span data-ttu-id="29921-155">Esses objetos normalmente incluem os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="29921-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="29921-156">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="29921-156">Resource Name</span></span>                                          | <span data-ttu-id="29921-157">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="29921-157">Required or Optional</span></span> | <span data-ttu-id="29921-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="29921-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="29921-159">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="29921-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="29921-160">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29921-160">Required.</span></span>            | <span data-ttu-id="29921-161">Contém os dados.</span><span class="sxs-lookup"><span data-stu-id="29921-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="29921-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29921-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29921-163">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="29921-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



