---
description: '\_serviço de \_ tipo de conteúdo WPD \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922384"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="82d46-103">\_serviço de \_ tipo de conteúdo WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="82d46-104">Um objeto que descreve seu tipo de \_ serviço de tipo de conteúdo WPD \_ \_ representa um serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82d46-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="82d46-105">Esse tipo de objeto dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="82d46-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="82d46-106">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="82d46-106">Property Name</span></span>                                                                                        | <span data-ttu-id="82d46-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="82d46-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="82d46-108">\_ID de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="82d46-109">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="82d46-109">Required, read-only.</span></span> <span data-ttu-id="82d46-110">Um cliente não pode definir essa propriedade, mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="82d46-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="82d46-111">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="82d46-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="82d46-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="82d46-113">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="82d46-114">Necessário se o objeto representar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="82d46-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="82d46-115">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="82d46-116">Obrigatório, somente leitura.</span><span class="sxs-lookup"><span data-stu-id="82d46-116">Required, read-only.</span></span> <span data-ttu-id="82d46-117">Um cliente não pode definir essa propriedade, mesmo no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="82d46-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="82d46-118">objeto WPD- \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="82d46-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="82d46-119">Necessário se o serviço não deve ser mostrado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="82d46-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="82d46-120">IsSystem de \_ objetos WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="82d46-121">Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="82d46-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="82d46-122">\_categoria de \_ objeto \_ funcional WPD</span><span class="sxs-lookup"><span data-stu-id="82d46-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="82d46-123">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="82d46-123">Required.</span></span> <span data-ttu-id="82d46-124">Isso representa o tipo de serviço do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82d46-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="82d46-125">\_versão do serviço WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="82d46-126">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="82d46-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="82d46-127">\_tipo de armazenamento WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="82d46-128">Necessário se o serviço for usado para armazenar objetos.</span><span class="sxs-lookup"><span data-stu-id="82d46-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="82d46-129">\_capacidade de armazenamento WPD \_</span><span class="sxs-lookup"><span data-stu-id="82d46-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="82d46-130">Necessário se o serviço for usado para armazenar objetos.</span><span class="sxs-lookup"><span data-stu-id="82d46-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="82d46-131">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="82d46-131">Typical Resources</span></span>

<span data-ttu-id="82d46-132">Esses objetos não hospedam recursos.</span><span class="sxs-lookup"><span data-stu-id="82d46-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82d46-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82d46-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d46-134">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="82d46-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



