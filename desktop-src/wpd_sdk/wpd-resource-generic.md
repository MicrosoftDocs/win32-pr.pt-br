---
description: Especifica um tipo de recurso que não foi definido de outra forma por dispositivos portáteis do Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090270"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="c8937-103">recurso de WPD \_ \_ genérico</span><span class="sxs-lookup"><span data-stu-id="c8937-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="c8937-104">Especifica um tipo de recurso que não foi definido de outra forma por dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="c8937-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="c8937-105">Você pode definir seus próprios recursos personalizados que dão suporte a qualquer atributo personalizado ou do Windows com dispositivos portáteis definidos.</span><span class="sxs-lookup"><span data-stu-id="c8937-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="c8937-106">No entanto, qualquer recurso que você criar deve dar suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="c8937-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="c8937-107">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="c8937-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="c8937-108">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="c8937-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c8937-109">\_ \_ Tamanho total do atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c8937-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="c8937-110">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c8937-110">Required.</span></span>                                              |
| [<span data-ttu-id="c8937-111">o \_ atributo de recurso WPD \_ \_ pode \_ ler</span><span class="sxs-lookup"><span data-stu-id="c8937-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="c8937-112">Necessário se os clientes puderem ler este recurso.</span><span class="sxs-lookup"><span data-stu-id="c8937-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="c8937-113">o \_ atributo de recurso WPD \_ \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="c8937-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="c8937-114">Necessário se os clientes puderem gravar nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="c8937-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="c8937-115">o \_ atributo de recurso WPD \_ \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="c8937-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="c8937-116">Necessário se os clientes puderem excluir esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c8937-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="c8937-117">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_</span><span class="sxs-lookup"><span data-stu-id="c8937-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="c8937-118">Necessário se os clientes tiverem acesso de leitura ao recurso.</span><span class="sxs-lookup"><span data-stu-id="c8937-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="c8937-119">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_</span><span class="sxs-lookup"><span data-stu-id="c8937-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="c8937-120">Necessário se os clientes tiverem acesso de gravação ao recurso.</span><span class="sxs-lookup"><span data-stu-id="c8937-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="c8937-121">\_formato de \_ atributo de recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="c8937-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="c8937-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c8937-122">Required.</span></span>                                              |
| [<span data-ttu-id="c8937-123">\_chave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c8937-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="c8937-124">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="c8937-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="c8937-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8937-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8937-126">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="c8937-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



