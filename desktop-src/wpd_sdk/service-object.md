---
description: Objeto de serviço
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837215"
---
# <a name="service-object"></a><span data-ttu-id="80221-103">Objeto de serviço</span><span class="sxs-lookup"><span data-stu-id="80221-103">Service Object</span></span>

<span data-ttu-id="80221-104">O objeto de serviço deve dar suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="80221-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="80221-105">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="80221-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="80221-106">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="80221-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80221-107">[\_ID de objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="80221-108">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="80221-108">Required.</span></span> <span data-ttu-id="80221-109">.</span><span class="sxs-lookup"><span data-stu-id="80221-109">.</span></span>                                                                           |
| <span data-ttu-id="80221-110">[\_ \_ ID pai do objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="80221-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="80221-111">Required.</span></span>                                                                             |
| <span data-ttu-id="80221-112">[\_nome do objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="80221-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="80221-113">Required.</span></span>                                                                             |
| <span data-ttu-id="80221-114">[\_ \_ \_ ID exclusiva persistente do objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="80221-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="80221-115">Required.</span></span>                                                                             |
| <span data-ttu-id="80221-116">[objeto WPD- \_ \_ oculto](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="80221-117">Necessário se o objeto de serviço não deve ser mostrado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="80221-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="80221-118">[IsSystem de \_ objetos WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="80221-119">Necessário se o objeto for um objeto do sistema (por exemplo, representa um arquivo do sistema).</span><span class="sxs-lookup"><span data-stu-id="80221-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="80221-120">[\_categoria de \_ objeto \_ funcional WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="80221-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="80221-121">Required.</span></span> <span data-ttu-id="80221-122">Isso representa o tipo de serviço do dispositivo, como contatos de serviço.</span><span class="sxs-lookup"><span data-stu-id="80221-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="80221-123">[\_versão do serviço WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="80221-124">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="80221-124">Required.</span></span>                                                                             |
| <span data-ttu-id="80221-125">[\_tipo de armazenamento WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="80221-126">Necessário se o serviço for usado para armazenar objetos.</span><span class="sxs-lookup"><span data-stu-id="80221-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="80221-127">[\_capacidade de armazenamento WPD \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80221-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="80221-128">Necessário se o serviço for usado para armazenar objetos.</span><span class="sxs-lookup"><span data-stu-id="80221-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="80221-129">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="80221-129">Typical Resources</span></span>

<span data-ttu-id="80221-130">Normalmente, esses objetos não hospedam recursos.</span><span class="sxs-lookup"><span data-stu-id="80221-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="80221-131">Formatos típicos</span><span class="sxs-lookup"><span data-stu-id="80221-131">Typical Formats</span></span>

<span data-ttu-id="80221-132">A lista a seguir identifica os formatos típicos usados pelo objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="80221-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="80221-133">No entanto, esse objeto não está limitado a esses formatos.</span><span class="sxs-lookup"><span data-stu-id="80221-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="80221-134">\_formato de objeto WPD \_ \_ não especificado</span><span class="sxs-lookup"><span data-stu-id="80221-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="80221-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80221-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80221-136">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="80221-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 
