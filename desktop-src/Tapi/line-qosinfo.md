---
description: A mensagem TSPI LINE \_ QOSINFO faz com que a TAPI dispare um evento de QoS. Consulte ITQOSEvent para obter informações adicionais.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Mensagem de LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783364"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="26d18-104">Mensagem de QOSINFO de linha \_</span><span class="sxs-lookup"><span data-stu-id="26d18-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="26d18-105">A mensagem TSPI **line \_ QOSINFO** faz com que a TAPI dispare um evento de QoS.</span><span class="sxs-lookup"><span data-stu-id="26d18-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="26d18-106">Consulte [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="26d18-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="26d18-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26d18-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d18-108">*htLine*</span><span class="sxs-lookup"><span data-stu-id="26d18-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="26d18-109">O identificador TAPI para a linha.</span><span class="sxs-lookup"><span data-stu-id="26d18-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="26d18-110">*htCall*</span><span class="sxs-lookup"><span data-stu-id="26d18-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="26d18-111">O identificador TAPI para a chamada.</span><span class="sxs-lookup"><span data-stu-id="26d18-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="26d18-112">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="26d18-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="26d18-113">A linha de valor \_ QOSINFO.</span><span class="sxs-lookup"><span data-stu-id="26d18-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="26d18-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="26d18-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="26d18-115">Um membro do enumerador de [**\_ eventos de QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) que identifica o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="26d18-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="26d18-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="26d18-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="26d18-117">Uma constante de [tipo de mídia](./tapiprotocol--constants.md) que identifica a mídia da chamada associada a esse evento.</span><span class="sxs-lookup"><span data-stu-id="26d18-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="26d18-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="26d18-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="26d18-119">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="26d18-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26d18-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d18-120">Requirements</span></span>



| <span data-ttu-id="26d18-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d18-121">Requirement</span></span> | <span data-ttu-id="26d18-122">Valor</span><span class="sxs-lookup"><span data-stu-id="26d18-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="26d18-123">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="26d18-123">TAPI version</span></span><br/> | <span data-ttu-id="26d18-124">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="26d18-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="26d18-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26d18-125">Header</span></span><br/>       | <dl> <span data-ttu-id="26d18-126"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d18-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26d18-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="26d18-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d18-128">**evento de QOS \_**</span><span class="sxs-lookup"><span data-stu-id="26d18-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="26d18-129">**ITQOSEvent**</span><span class="sxs-lookup"><span data-stu-id="26d18-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

