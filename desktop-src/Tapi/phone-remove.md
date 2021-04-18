---
description: A \_ mensagem de remoção de telefone TAPI é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de telefone.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Mensagem de PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760332"
---
# <a name="phone_remove-message"></a><span data-ttu-id="a2ac1-103">\_Remover mensagem de telefone</span><span class="sxs-lookup"><span data-stu-id="a2ac1-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="a2ac1-104">A mensagem **de \_ remoção de telefone** TAPI é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="a2ac1-105">Em geral, isso não é usado para remoções temporárias, como a extração de dispositivos PCMCIA, mas apenas para remoções permanentes nas quais o dispositivo não seria mais relatado pelo provedor de serviços se a TAPI fosse reinicializada.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a2ac1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ac1-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a2ac1-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ac1-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-108">Reserved.</span></span> <span data-ttu-id="a2ac1-109">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a2ac1-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a2ac1-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ac1-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-111">Reserved.</span></span> <span data-ttu-id="a2ac1-112">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a2ac1-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a2ac1-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ac1-114">Identificador do dispositivo de telefone que foi removido.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="a2ac1-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a2ac1-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ac1-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-116">Reserved.</span></span> <span data-ttu-id="a2ac1-117">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a2ac1-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a2ac1-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ac1-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-119">Reserved.</span></span> <span data-ttu-id="a2ac1-120">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ac1-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2ac1-121">Return value</span></span>

<span data-ttu-id="a2ac1-122">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ac1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2ac1-123">Remarks</span></span>

<span data-ttu-id="a2ac1-124">Os aplicativos da TAPI versão 2,0 ou posterior são enviados uma mensagem de **\_ remoção de telefone** .</span><span class="sxs-lookup"><span data-stu-id="a2ac1-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="a2ac1-125">Isso informa que o dispositivo foi removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="a2ac1-126">A mensagem de **\_ remoção de telefone** é precedida por uma mensagem de [**\_ fechamento de telefone**](phone-close.md) em cada identificador de telefone, se o aplicativo tiver o telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="a2ac1-127">Essa mensagem é enviada para todos os aplicativos que dão suporte à TAPI versão 2,0 ou posterior que tenha chamado [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), incluindo aqueles que não têm dispositivos de telefone abertos no momento.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="a2ac1-128">Os aplicativos mais antigos (que negociaram a TAPI versão 1,4 ou anterior) recebem uma mensagem de [**\_ estado de telefone**](phone-state.md) que especifica o PHONESTATE \_ removido, seguido por uma mensagem de [**\_ fechamento de telefone**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ac1-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="a2ac1-129">Ao contrário da mensagem de **\_ remoção de telefone** , no entanto, esses aplicativos mais antigos podem receber essas mensagens somente se tiverem o telefone aberto quando ele for removido.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="a2ac1-130">Se eles não tiverem o telefone aberto, sua única indicação de que o dispositivo foi removido estaria recebendo um PHONEERR \_ nodevice quando ele tentar acessar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="a2ac1-131">Depois que um dispositivo for removido, qualquer tentativa de acessar o dispositivo pelo identificador de dispositivo resultará em um \_ erro NOdevice do PHONEERR.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="a2ac1-132">Depois que todos os aplicativos TAPI tiverem sido desligados para que a TAPI possa ser reiniciada e quando a TAPI for reinicializada, o dispositivo removido não ocupará mais um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="a2ac1-133">Implementação: é a TAPI que retorna essa mensagem do PHONEERR \_ nodevice depois que uma \_ mensagem de remoção de telefone é recebida de um provedor de serviços; nenhuma chamada adicional é feita ao provedor de serviços usando esse identificador de dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="a2ac1-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2ac1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ac1-134">Requirements</span></span>



| <span data-ttu-id="a2ac1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ac1-135">Requirement</span></span> | <span data-ttu-id="a2ac1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ac1-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a2ac1-137">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a2ac1-137">TAPI version</span></span><br/> | <span data-ttu-id="a2ac1-138">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a2ac1-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a2ac1-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2ac1-139">Header</span></span><br/>       | <dl> <span data-ttu-id="a2ac1-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ac1-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ac1-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2ac1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ac1-142">**\_fechar telefone**</span><span class="sxs-lookup"><span data-stu-id="a2ac1-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="a2ac1-143">**Estado do telefone \_**</span><span class="sxs-lookup"><span data-stu-id="a2ac1-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="a2ac1-144">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="a2ac1-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="a2ac1-145">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="a2ac1-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




