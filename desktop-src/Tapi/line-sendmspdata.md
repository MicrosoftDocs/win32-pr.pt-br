---
description: A mensagem de SENDMSPDATA da linha TSPI \_ é enviada quando o provedor de serviços de telefonia (TSP) deseja passar informações para o MSP (provedor de serviços de mídia).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Mensagem de LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761354"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="e0034-103">Mensagem de SENDMSPDATA de linha \_</span><span class="sxs-lookup"><span data-stu-id="e0034-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="e0034-104">A mensagem **de \_ SENDMSPDATA da linha** TSPI é enviada quando o provedor de serviços de telefonia (TSP) deseja passar informações para o MSP (provedor de serviços de mídia).</span><span class="sxs-lookup"><span data-stu-id="e0034-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e0034-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0034-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0034-106">*htLine*</span><span class="sxs-lookup"><span data-stu-id="e0034-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-107">O identificador TAPI para a linha.</span><span class="sxs-lookup"><span data-stu-id="e0034-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="e0034-108">*htCall*</span><span class="sxs-lookup"><span data-stu-id="e0034-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-109">O identificador TAPI para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e0034-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="e0034-110">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="e0034-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-111">A linha de valor \_ SENDMSPDATA.</span><span class="sxs-lookup"><span data-stu-id="e0034-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="e0034-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e0034-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-113">Identifica o MSP que deve receber a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0034-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="e0034-114">Se for 0, a mensagem será enviada a todos os MSPs.</span><span class="sxs-lookup"><span data-stu-id="e0034-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="e0034-115">Esse é o identificador que é passado para a função [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .</span><span class="sxs-lookup"><span data-stu-id="e0034-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="e0034-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e0034-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-117">O buffer a ser passado para o MSP.</span><span class="sxs-lookup"><span data-stu-id="e0034-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="e0034-118">O buffer não é interpretado pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="e0034-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="e0034-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e0034-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-120">O tamanho, em bytes, do buffer em *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="e0034-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0034-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0034-121">Remarks</span></span>

<span data-ttu-id="e0034-122">O provedor de serviços deve negociar uma TAPI versão 3,0 ou posterior para que essa mensagem opere.</span><span class="sxs-lookup"><span data-stu-id="e0034-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0034-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0034-123">Requirements</span></span>



| <span data-ttu-id="e0034-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0034-124">Requirement</span></span> | <span data-ttu-id="e0034-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e0034-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e0034-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e0034-126">TAPI version</span></span><br/> | <span data-ttu-id="e0034-127">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="e0034-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="e0034-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0034-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e0034-129"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0034-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0034-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0034-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0034-131">Sobre o MSP (provedor de serviços de mídia)</span><span class="sxs-lookup"><span data-stu-id="e0034-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="e0034-132">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="e0034-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="e0034-133">**TSPI \_ LineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="e0034-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="e0034-134">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="e0034-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="e0034-135">**TSPI \_ lineRecieveMSPData**</span><span class="sxs-lookup"><span data-stu-id="e0034-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="e0034-136">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="e0034-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

