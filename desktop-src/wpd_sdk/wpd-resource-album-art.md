---
description: Especifica uma imagem que representa a arte-final do álbum do objeto.
ms.assetid: 7a31ebb6-c4ab-4899-9c2e-c960aac4f0f9
title: WPD_RESOURCE_ALBUM_ART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4b800aa2ae22f2400f3195b85da6bd3bd35b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501606"
---
# <a name="wpd_resource_album_art"></a><span data-ttu-id="72ece-103">\_arte do \_ álbum de recursos WPD \_</span><span class="sxs-lookup"><span data-stu-id="72ece-103">WPD\_RESOURCE\_ALBUM\_ART</span></span>

<span data-ttu-id="72ece-104">Especifica uma imagem que representa a arte-final do álbum do objeto.</span><span class="sxs-lookup"><span data-stu-id="72ece-104">Specifies an image that represents the album artwork for the object.</span></span>

<span data-ttu-id="72ece-105">Esse tipo de recurso deve dar suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="72ece-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="72ece-106">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="72ece-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="72ece-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="72ece-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="72ece-108">\_largura de mídia WPD \_</span><span class="sxs-lookup"><span data-stu-id="72ece-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="72ece-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="72ece-109">Required.</span></span>                                              |
| [<span data-ttu-id="72ece-110">\_altura de mídia WPD \_</span><span class="sxs-lookup"><span data-stu-id="72ece-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="72ece-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="72ece-111">Required.</span></span>                                              |
| [<span data-ttu-id="72ece-112">\_ \_ Tamanho total do atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="72ece-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="72ece-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="72ece-113">Required.</span></span>                                              |
| [<span data-ttu-id="72ece-114">o \_ atributo de recurso WPD \_ \_ pode \_ ler</span><span class="sxs-lookup"><span data-stu-id="72ece-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="72ece-115">Necessário se os clientes puderem ler este recurso.</span><span class="sxs-lookup"><span data-stu-id="72ece-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="72ece-116">o \_ atributo de recurso WPD \_ \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="72ece-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="72ece-117">Necessário se os clientes puderem gravar nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="72ece-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="72ece-118">o \_ atributo de recurso WPD \_ \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="72ece-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="72ece-119">Necessário se os clientes puderem excluir esse recurso.</span><span class="sxs-lookup"><span data-stu-id="72ece-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="72ece-120">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_</span><span class="sxs-lookup"><span data-stu-id="72ece-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="72ece-121">Necessário se os clientes tiverem acesso de leitura ao recurso.</span><span class="sxs-lookup"><span data-stu-id="72ece-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="72ece-122">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_</span><span class="sxs-lookup"><span data-stu-id="72ece-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="72ece-123">Necessário se os clientes tiverem acesso de gravação ao recurso.</span><span class="sxs-lookup"><span data-stu-id="72ece-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="72ece-124">\_formato de \_ atributo de recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="72ece-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="72ece-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="72ece-125">Required.</span></span>                                              |
| [<span data-ttu-id="72ece-126">\_chave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="72ece-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="72ece-127">Recomendadas</span><span class="sxs-lookup"><span data-stu-id="72ece-127">Recommended</span></span>                                            |



 

## <a name="see-also"></a><span data-ttu-id="72ece-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="72ece-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ece-129">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="72ece-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



