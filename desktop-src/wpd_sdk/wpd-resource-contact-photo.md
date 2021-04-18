---
description: Especifica uma imagem que representa uma foto do indivíduo referenciado no objeto de contato.
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780241"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="54f1e-103">\_foto de \_ contato de recursos WPD \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="54f1e-104">Especifica uma imagem que representa uma foto do indivíduo referenciado no objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="54f1e-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="54f1e-105">Esse tipo de recurso deve dar suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="54f1e-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="54f1e-106">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="54f1e-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="54f1e-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="54f1e-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="54f1e-108">\_largura de mídia WPD \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="54f1e-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="54f1e-109">Required.</span></span>                                              |
| [<span data-ttu-id="54f1e-110">\_altura de mídia WPD \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="54f1e-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="54f1e-111">Required.</span></span>                                              |
| [<span data-ttu-id="54f1e-112">\_ \_ Tamanho total do atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="54f1e-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="54f1e-113">Required.</span></span>                                              |
| [<span data-ttu-id="54f1e-114">o \_ atributo de recurso WPD \_ \_ pode \_ ler</span><span class="sxs-lookup"><span data-stu-id="54f1e-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="54f1e-115">Necessário se os clientes puderem ler este recurso.</span><span class="sxs-lookup"><span data-stu-id="54f1e-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="54f1e-116">o \_ atributo de recurso WPD \_ \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="54f1e-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="54f1e-117">Necessário se os clientes puderem gravar nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="54f1e-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="54f1e-118">o \_ atributo de recurso WPD \_ \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="54f1e-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="54f1e-119">Necessário se os clientes puderem excluir esse recurso.</span><span class="sxs-lookup"><span data-stu-id="54f1e-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="54f1e-120">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="54f1e-121">Necessário se os clientes tiverem acesso de leitura ao recurso.</span><span class="sxs-lookup"><span data-stu-id="54f1e-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="54f1e-122">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="54f1e-123">Necessário se os clientes tiverem acesso de gravação ao recurso.</span><span class="sxs-lookup"><span data-stu-id="54f1e-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="54f1e-124">\_formato de \_ atributo de recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="54f1e-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="54f1e-125">Required.</span></span>                                              |
| [<span data-ttu-id="54f1e-126">\_chave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="54f1e-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="54f1e-127">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="54f1e-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="54f1e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="54f1e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f1e-129">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="54f1e-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



