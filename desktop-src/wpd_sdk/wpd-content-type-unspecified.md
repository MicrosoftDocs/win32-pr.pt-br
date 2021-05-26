---
description: TIPO DE CONTEÚDO WPD \_ \_ NÃO \_ ESPECIFICADO
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423676"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="df8f2-103">TIPO DE CONTEÚDO WPD \_ \_ NÃO \_ ESPECIFICADO</span><span class="sxs-lookup"><span data-stu-id="df8f2-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="df8f2-104">Um objeto que descreve seu tipo como WPD \_ CONTENT \_ TYPE UNSPECIFIED representa um objeto genérico que pode ou não ter \_ um arquivo físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="df8f2-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="df8f2-105">A diferença entre esse tipo e WPD CONTENT TYPE GENERIC FILE é que os objetos WPD CONTENT TYPE GENERIC FILE devem \_ ter um arquivo \_ físico \_ \_ \_ \_ \_ \_ subjacente.</span><span class="sxs-lookup"><span data-stu-id="df8f2-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="df8f2-106">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="df8f2-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="df8f2-107">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="df8f2-107">Property Name</span></span>       | <span data-ttu-id="df8f2-108">Obrigatório ou Opcional</span><span class="sxs-lookup"><span data-stu-id="df8f2-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="df8f2-109">ID DO \_ \_ OBJETO WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="df8f2-110">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df8f2-110">Required, read-only.</span></span> <span data-ttu-id="df8f2-111">Um cliente não pode definir essa propriedade mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="df8f2-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="df8f2-112">ID PAI \_ \_ DO OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="df8f2-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="df8f2-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-114">NOME DO OBJETO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="df8f2-115">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="df8f2-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="df8f2-116">ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="df8f2-117">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df8f2-117">Required, read-only.</span></span> <span data-ttu-id="df8f2-118">Um cliente não pode definir essa propriedade mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="df8f2-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="df8f2-119">FORMATO DE OBJETO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="df8f2-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="df8f2-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-121">TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="df8f2-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="df8f2-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-123">\_ \_ ISHIDDEN DE OBJETO WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="df8f2-124">Necessário se o objeto estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="df8f2-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="df8f2-125">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="df8f2-126">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="df8f2-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="df8f2-127">\_tamanho do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="df8f2-128">Necessário se o objeto tiver pelo menos um recurso.</span><span class="sxs-lookup"><span data-stu-id="df8f2-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="df8f2-129">\_nome de \_ \_ arquivo original do objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="df8f2-130">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="df8f2-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="df8f2-131">\_objeto WPD \_ não \_ consumível</span><span class="sxs-lookup"><span data-stu-id="df8f2-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="df8f2-132">Recomendado se o objeto não for destinada ao consumo pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df8f2-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="df8f2-133">\_referências de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="df8f2-134">Obrigatório se o objeto tiver referências a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="df8f2-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="df8f2-135">\_ \_ palavras-chave do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="df8f2-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-137">\_ID de \_ sincronização do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="df8f2-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-139">o \_ objeto \_ WPD \_ é \_ protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="df8f2-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="df8f2-140">Necessário se o objeto estiver protegido pela tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="df8f2-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="df8f2-141">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="df8f2-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="df8f2-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-143">\_data do objeto WPD \_ \_ modificado</span><span class="sxs-lookup"><span data-stu-id="df8f2-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="df8f2-144">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="df8f2-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="df8f2-145">\_data do objeto WPD \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="df8f2-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="df8f2-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-147">\_referências de \_ retorno de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="df8f2-148">Recomendado se o objeto for referenciado por outro objeto.</span><span class="sxs-lookup"><span data-stu-id="df8f2-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="df8f2-149">\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="df8f2-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="df8f2-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-151">OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO</span><span class="sxs-lookup"><span data-stu-id="df8f2-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="df8f2-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="df8f2-153">O OBJETO WPD \_ \_ PODE \_ EXCLUIR</span><span class="sxs-lookup"><span data-stu-id="df8f2-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="df8f2-154">Necessário se o objeto não puder ser excluído.</span><span class="sxs-lookup"><span data-stu-id="df8f2-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="df8f2-155">LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="df8f2-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="df8f2-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df8f2-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="df8f2-157">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="df8f2-157">Typical Resources</span></span>

<span data-ttu-id="df8f2-158">Esses objetos normalmente incluem os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="df8f2-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="df8f2-159">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="df8f2-159">Resource Name</span></span>                                          | <span data-ttu-id="df8f2-160">Obrigatório ou Opcional</span><span class="sxs-lookup"><span data-stu-id="df8f2-160">Required or Optional</span></span>                             | <span data-ttu-id="df8f2-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="df8f2-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="df8f2-162">**WPD \_ RESOURCE \_ DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="df8f2-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="df8f2-163">Necessário se o objeto for apoiado por dados binários.</span><span class="sxs-lookup"><span data-stu-id="df8f2-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="df8f2-164">Contém os dados binários.</span><span class="sxs-lookup"><span data-stu-id="df8f2-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df8f2-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df8f2-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df8f2-166">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="df8f2-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



