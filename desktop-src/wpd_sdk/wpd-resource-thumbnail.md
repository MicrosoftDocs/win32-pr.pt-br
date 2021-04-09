---
description: Especifica uma pequena imagem&\# 8212; normalmente uma versão menor de uma imagem maior no objeto.
ms.assetid: ad1eac9d-b182-49b2-bd2c-2d76e2026d80
title: WPD_RESOURCE_THUMBNAIL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc26af624f756f55ccb10ccf3f8c7bf3e6a6035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090269"
---
# <a name="wpd_resource_thumbnail"></a><span data-ttu-id="e6deb-103">\_miniatura do recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-103">WPD\_RESOURCE\_THUMBNAIL</span></span>

<span data-ttu-id="e6deb-104">Especifica uma imagem pequena — normalmente uma versão menor de uma imagem maior no objeto.</span><span class="sxs-lookup"><span data-stu-id="e6deb-104">Specifies a small picture—typically a smaller version of a larger picture in the object.</span></span>

<span data-ttu-id="e6deb-105">Esse tipo de recurso deve dar suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="e6deb-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="e6deb-106">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="e6deb-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="e6deb-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="e6deb-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e6deb-108">\_largura de mídia WPD \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="e6deb-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e6deb-109">Required.</span></span>                                              |
| [<span data-ttu-id="e6deb-110">\_altura de mídia WPD \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="e6deb-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e6deb-111">Required.</span></span>                                              |
| [<span data-ttu-id="e6deb-112">\_ \_ Tamanho total do atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="e6deb-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e6deb-113">Required.</span></span>                                              |
| [<span data-ttu-id="e6deb-114">o \_ atributo de recurso WPD \_ \_ pode \_ ler</span><span class="sxs-lookup"><span data-stu-id="e6deb-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="e6deb-115">Necessário se os clientes puderem ler este recurso.</span><span class="sxs-lookup"><span data-stu-id="e6deb-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="e6deb-116">o \_ atributo de recurso WPD \_ \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="e6deb-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="e6deb-117">Necessário se os clientes puderem gravar nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="e6deb-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="e6deb-118">o \_ atributo de recurso WPD \_ \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="e6deb-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="e6deb-119">Necessário se os clientes puderem excluir esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e6deb-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="e6deb-120">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="e6deb-121">Necessário se os clientes tiverem acesso de leitura ao recurso.</span><span class="sxs-lookup"><span data-stu-id="e6deb-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="e6deb-122">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="e6deb-123">Necessário se os clientes tiverem acesso de gravação ao recurso.</span><span class="sxs-lookup"><span data-stu-id="e6deb-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="e6deb-124">\_formato de \_ atributo de recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="e6deb-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e6deb-125">Required.</span></span>                                              |
| [<span data-ttu-id="e6deb-126">\_chave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="e6deb-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="e6deb-127">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="e6deb-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="e6deb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6deb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6deb-129">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="e6deb-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



