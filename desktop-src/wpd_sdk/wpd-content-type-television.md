---
description: Um objeto que descreve seu tipo como a \_ televisão do tipo de conteúdo WPD \_ \_ representa uma gravação de televisão.
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297125"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="3b446-103">\_televisão de \_ tipo de conteúdo WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="3b446-104">Um objeto que descreve seu tipo como a \_ televisão do tipo de conteúdo WPD \_ \_ representa uma gravação de televisão.</span><span class="sxs-lookup"><span data-stu-id="3b446-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="3b446-105">Esse tipo de objeto deve hospedar as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b446-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="3b446-106">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="3b446-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="3b446-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="3b446-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="3b446-108">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="3b446-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3b446-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="3b446-110">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="3b446-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3b446-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="3b446-112">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="3b446-113">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3b446-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="3b446-114">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="3b446-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3b446-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="3b446-116">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="3b446-117">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3b446-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="3b446-118">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="3b446-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3b446-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="3b446-120">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="3b446-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="3b446-121">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="3b446-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="3b446-122">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="3b446-123">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="3b446-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="3b446-124">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="3b446-125">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="3b446-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="3b446-126">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="3b446-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="3b446-127">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3b446-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="3b446-128">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="3b446-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="3b446-129">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b446-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="3b446-130">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="3b446-131">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="3b446-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="3b446-132">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="3b446-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="3b446-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-134">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="3b446-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-136">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="3b446-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="3b446-137">Necessário se o objeto for protegido pela tecnologia de Rights Management digital.</span><span class="sxs-lookup"><span data-stu-id="3b446-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="3b446-138">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="3b446-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="3b446-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-140">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="3b446-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="3b446-141">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="3b446-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="3b446-142">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="3b446-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="3b446-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-144">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="3b446-145">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="3b446-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="3b446-146">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="3b446-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-148">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="3b446-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="3b446-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-150">o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso</span><span class="sxs-lookup"><span data-stu-id="3b446-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="3b446-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b446-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="3b446-152">o \_ objeto WPD \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="3b446-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="3b446-153">Obrigatório se o objeto não puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3b446-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="3b446-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="3b446-154">Typical Resources</span></span>

<span data-ttu-id="3b446-155">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3b446-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b446-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b446-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b446-157">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="3b446-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



