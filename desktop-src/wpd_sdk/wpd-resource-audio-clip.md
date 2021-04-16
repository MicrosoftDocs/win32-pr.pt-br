---
description: Especifica um clipe de áudio para o objeto.
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779502"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="0970b-103">\_clipe de \_ áudio de recursos WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="0970b-104">Especifica um clipe de áudio para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0970b-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="0970b-105">Esse tipo de recurso deve dar suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="0970b-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="0970b-106">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="0970b-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="0970b-107">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="0970b-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0970b-108">taxa de bits de \_ áudio WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="0970b-109">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="0970b-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="0970b-110">\_contagem de \_ canais de áudio WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="0970b-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0970b-111">Optional.</span></span>                                              |
| [<span data-ttu-id="0970b-112">\_código de \_ formato de áudio WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="0970b-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0970b-113">Optional.</span></span>                                              |
| [<span data-ttu-id="0970b-114">\_profundidade de \_ bit de áudio WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="0970b-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0970b-115">Optional.</span></span>                                              |
| [<span data-ttu-id="0970b-116">\_alinhamento de \_ bloco de áudio WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="0970b-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0970b-117">Optional.</span></span>                                              |
| [<span data-ttu-id="0970b-118">\_ \_ Tamanho total do atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="0970b-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="0970b-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0970b-119">Required.</span></span>                                              |
| [<span data-ttu-id="0970b-120">o \_ atributo de recurso WPD \_ \_ pode \_ ler</span><span class="sxs-lookup"><span data-stu-id="0970b-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="0970b-121">Necessário se os clientes puderem ler este recurso.</span><span class="sxs-lookup"><span data-stu-id="0970b-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="0970b-122">o \_ atributo de recurso WPD \_ \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="0970b-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="0970b-123">Necessário se os clientes puderem gravar nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="0970b-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="0970b-124">o \_ atributo de recurso WPD \_ \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="0970b-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="0970b-125">Necessário se os clientes puderem excluir esse recurso.</span><span class="sxs-lookup"><span data-stu-id="0970b-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="0970b-126">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_</span><span class="sxs-lookup"><span data-stu-id="0970b-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="0970b-127">Necessário se os clientes tiverem acesso de leitura ao recurso.</span><span class="sxs-lookup"><span data-stu-id="0970b-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="0970b-128">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_</span><span class="sxs-lookup"><span data-stu-id="0970b-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="0970b-129">Necessário se os clientes tiverem acesso de gravação ao recurso.</span><span class="sxs-lookup"><span data-stu-id="0970b-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="0970b-130">\_formato de \_ atributo de recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="0970b-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="0970b-131">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0970b-131">Required.</span></span>                                              |
| [<span data-ttu-id="0970b-132">\_chave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="0970b-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="0970b-133">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="0970b-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="0970b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0970b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0970b-135">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="0970b-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



