---
title: Constantes do coletor de eventos do Windows (Evcoll. h)
description: O SDK do coletor de eventos do Windows contém as seguintes constantes.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644210"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="f3b72-103">Constantes do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="f3b72-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="f3b72-104">O SDK do coletor de eventos do Windows contém as seguintes constantes.</span><span class="sxs-lookup"><span data-stu-id="f3b72-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="f3b72-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_máscara de \_ tipo de variante do EC \_**</span><span class="sxs-lookup"><span data-stu-id="f3b72-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="f3b72-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-107">Usado para mascarar o bit da matriz da propriedade **Type** de uma [**\_ variante do EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) para extrair o tipo do valor da variante.</span><span class="sxs-lookup"><span data-stu-id="f3b72-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3b72-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_matriz de \_ tipo de variante do EC \_**</span><span class="sxs-lookup"><span data-stu-id="f3b72-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-109">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="f3b72-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-110">Quando esse bit é definido na propriedade **Type** de uma [**\_ variante do EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), a variante contém um ponteiro para uma matriz de valores, em vez do próprio valor.</span><span class="sxs-lookup"><span data-stu-id="f3b72-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3b72-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_acesso de leitura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="f3b72-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-112">1</span><span class="sxs-lookup"><span data-stu-id="f3b72-112">1</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-113">Permissão de controle de acesso de leitura que permite que informações sejam lidas do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f3b72-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3b72-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_acesso de gravação do EC \_**</span><span class="sxs-lookup"><span data-stu-id="f3b72-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-115">2</span><span class="sxs-lookup"><span data-stu-id="f3b72-115">2</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-116">Permissão de controle de acesso de gravação que permite que as informações sejam gravadas no coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f3b72-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3b72-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**\_sempre abrir o EC \_**</span><span class="sxs-lookup"><span data-stu-id="f3b72-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-118">0</span><span class="sxs-lookup"><span data-stu-id="f3b72-118">0</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-119">Abre uma assinatura existente ou cria a assinatura se ela não existir.</span><span class="sxs-lookup"><span data-stu-id="f3b72-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="f3b72-120">Usado pelo método [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="f3b72-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3b72-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**\_criar \_ novo EC**</span><span class="sxs-lookup"><span data-stu-id="f3b72-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-122">1</span><span class="sxs-lookup"><span data-stu-id="f3b72-122">1</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-123">Um sinalizador passado para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) especificando que uma nova assinatura deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="f3b72-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3b72-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ Open \_ existente**</span><span class="sxs-lookup"><span data-stu-id="f3b72-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b72-125">2</span><span class="sxs-lookup"><span data-stu-id="f3b72-125">2</span></span>
</dt> <dt>



<span data-ttu-id="f3b72-126">Um sinalizador passado para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) especificando que uma assinatura existente deve ser aberta.</span><span class="sxs-lookup"><span data-stu-id="f3b72-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3b72-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b72-127">Requirements</span></span>



| <span data-ttu-id="f3b72-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b72-128">Requirement</span></span> | <span data-ttu-id="f3b72-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b72-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b72-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b72-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b72-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3b72-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="f3b72-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b72-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b72-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3b72-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="f3b72-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3b72-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b72-135"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b72-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





