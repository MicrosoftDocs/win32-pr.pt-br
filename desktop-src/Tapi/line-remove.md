---
description: A mensagem de remoção de linha TAPI \_ é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de linha.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Mensagem de LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766218"
---
# <a name="line_remove-message"></a><span data-ttu-id="3236a-103">Mensagem de remoção de linha \_</span><span class="sxs-lookup"><span data-stu-id="3236a-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="3236a-104">A mensagem **de \_ remoção de linha** TAPI é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3236a-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="3236a-105">Em geral, isso não é usado para remoções temporárias, como a extração de dispositivos PCMCIA, mas apenas para remoções permanentes nas quais o dispositivo não seria mais relatado pelo provedor de serviços se a TAPI fosse reinicializada.</span><span class="sxs-lookup"><span data-stu-id="3236a-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3236a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3236a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3236a-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="3236a-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3236a-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3236a-108">Reserved.</span></span> <span data-ttu-id="3236a-109">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3236a-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3236a-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="3236a-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3236a-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3236a-111">Reserved.</span></span> <span data-ttu-id="3236a-112">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3236a-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3236a-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3236a-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3236a-114">Identificador do dispositivo de linha que foi removido.</span><span class="sxs-lookup"><span data-stu-id="3236a-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="3236a-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3236a-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3236a-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3236a-116">Reserved.</span></span> <span data-ttu-id="3236a-117">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3236a-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3236a-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3236a-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3236a-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3236a-119">Reserved.</span></span> <span data-ttu-id="3236a-120">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3236a-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3236a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3236a-121">Return value</span></span>

<span data-ttu-id="3236a-122">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3236a-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3236a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3236a-123">Remarks</span></span>

<span data-ttu-id="3236a-124">Os aplicativos que dão suporte à TAPI versão 2,0 ou posterior são enviados uma mensagem de **\_ remoção de linha** .</span><span class="sxs-lookup"><span data-stu-id="3236a-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="3236a-125">Isso informa que o dispositivo foi removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="3236a-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="3236a-126">A mensagem de **\_ remoção de linha** é precedida por uma mensagem de [**\_ fechamento de linha**](line-close.md) em cada alça de linha, se o aplicativo tivesse a linha aberta.</span><span class="sxs-lookup"><span data-stu-id="3236a-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="3236a-127">Essa mensagem é enviada para todos os aplicativos que dão suporte à TAPI versão 2,0 ou posterior que tenha chamado [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluindo aqueles que não têm dispositivos de linha abertos no momento.</span><span class="sxs-lookup"><span data-stu-id="3236a-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="3236a-128">Os aplicativos mais antigos são enviados uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) especificando LINEDEVSTATE \_ removido, seguido por uma mensagem de fechamento de linha \_ .</span><span class="sxs-lookup"><span data-stu-id="3236a-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="3236a-129">Ao contrário da mensagem de **\_ remoção de linha** , no entanto, esses aplicativos mais antigos podem receber essas mensagens somente se tiverem a linha aberta quando ela for removida.</span><span class="sxs-lookup"><span data-stu-id="3236a-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="3236a-130">Se eles não tiverem a linha aberta, sua única indicação de que o dispositivo foi removido estaria recebendo um \_ erro NODEVICE LINEERR ao tentar acessar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3236a-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="3236a-131">Depois que um dispositivo for removido, qualquer tentativa de acessar o dispositivo pelo identificador de dispositivo resultará em um \_ erro NOdevice do LINEERR.</span><span class="sxs-lookup"><span data-stu-id="3236a-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="3236a-132">Depois que todos os aplicativos TAPI tiverem sido desligados para que a TAPI possa ser reiniciada e quando a TAPI for reinicializada, o dispositivo removido não ocupará mais um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3236a-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="3236a-133">Implementação: é TAPI que retorna este LINEERR \_ nodevice; depois que uma mensagem de **\_ remoção de linha** é recebida de um provedor de serviços; nenhuma chamada adicional é feita ao provedor de serviços usando esse identificador de dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3236a-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3236a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3236a-134">Requirements</span></span>



| <span data-ttu-id="3236a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3236a-135">Requirement</span></span> | <span data-ttu-id="3236a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3236a-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3236a-137">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3236a-137">TAPI version</span></span><br/> | <span data-ttu-id="3236a-138">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3236a-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3236a-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3236a-139">Header</span></span><br/>       | <dl> <span data-ttu-id="3236a-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3236a-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3236a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3236a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3236a-142">**fechamento de linha \_**</span><span class="sxs-lookup"><span data-stu-id="3236a-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="3236a-143">**LINEDEVSTATE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="3236a-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="3236a-144">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="3236a-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




