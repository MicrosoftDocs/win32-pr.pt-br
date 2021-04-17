---
description: '\_calendário de \_ tipo de conteúdo WPD \_'
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782710"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="562f1-103">\_calendário de \_ tipo de conteúdo WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="562f1-104">Um objeto que descreve seu tipo de \_ calendário de tipo de conteúdo WPD \_ \_ representa um calendário.</span><span class="sxs-lookup"><span data-stu-id="562f1-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="562f1-105">O objeto pode ser um arquivo que contém informações de calendário ou uma pasta que contém outros objetos relacionados a calendário, como tarefas, compromissos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="562f1-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="562f1-106">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="562f1-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="562f1-107">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="562f1-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="562f1-108">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="562f1-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="562f1-109">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="562f1-110">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="562f1-110">Required.</span></span>                                                             |
| [<span data-ttu-id="562f1-111">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="562f1-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="562f1-112">Required.</span></span>                                                             |
| [<span data-ttu-id="562f1-113">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="562f1-114">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="562f1-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="562f1-115">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="562f1-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="562f1-116">Required.</span></span>                                                             |
| [<span data-ttu-id="562f1-117">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="562f1-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="562f1-118">Required.</span></span>                                                             |
| [<span data-ttu-id="562f1-119">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="562f1-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="562f1-120">Required.</span></span>                                                             |
| [<span data-ttu-id="562f1-121">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="562f1-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="562f1-122">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="562f1-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="562f1-123">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="562f1-124">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="562f1-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="562f1-125">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="562f1-126">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="562f1-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="562f1-127">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="562f1-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="562f1-128">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="562f1-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="562f1-129">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="562f1-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="562f1-130">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="562f1-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="562f1-131">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="562f1-132">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="562f1-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="562f1-133">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="562f1-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="562f1-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="562f1-135">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="562f1-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="562f1-137">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="562f1-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="562f1-138">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="562f1-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="562f1-139">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="562f1-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="562f1-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="562f1-141">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="562f1-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="562f1-142">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="562f1-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="562f1-143">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="562f1-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="562f1-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="562f1-145">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="562f1-146">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="562f1-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="562f1-147">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="562f1-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="562f1-149">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="562f1-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="562f1-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="562f1-151">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="562f1-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="562f1-152">Necessário se o objeto puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="562f1-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="562f1-153">\_localidade do \_ idioma do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="562f1-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="562f1-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="562f1-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="562f1-155">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="562f1-155">Typical Resources</span></span>

<span data-ttu-id="562f1-156">Esses objetos normalmente incluem os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="562f1-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="562f1-157">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="562f1-157">Resource Name</span></span>                                          | <span data-ttu-id="562f1-158">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="562f1-158">Required or Optional</span></span>                             | <span data-ttu-id="562f1-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="562f1-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="562f1-160">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="562f1-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="562f1-161">Necessário se o objeto for apoiado por dados binários.</span><span class="sxs-lookup"><span data-stu-id="562f1-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="562f1-162">Contém os dados.</span><span class="sxs-lookup"><span data-stu-id="562f1-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="562f1-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="562f1-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="562f1-164">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="562f1-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



