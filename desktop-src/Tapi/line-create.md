---
description: A mensagem TAPI \_ de criação de linha é enviada para informar o aplicativo sobre a criação de um novo dispositivo de linha.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Mensagem de LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782908"
---
# <a name="line_create-message"></a><span data-ttu-id="c3cee-103">LINHA \_ criar mensagem</span><span class="sxs-lookup"><span data-stu-id="c3cee-103">LINE\_CREATE message</span></span>

<span data-ttu-id="c3cee-104">A mensagem TAPI de **\_ criação de linha** é enviada para informar o aplicativo sobre a criação de um novo dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="c3cee-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c3cee-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3cee-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3cee-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="c3cee-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c3cee-107">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="c3cee-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c3cee-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="c3cee-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c3cee-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="c3cee-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c3cee-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c3cee-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c3cee-111">O *hDeviceID* do dispositivo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="c3cee-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="c3cee-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c3cee-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c3cee-113">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="c3cee-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c3cee-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c3cee-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c3cee-115">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="c3cee-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3cee-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3cee-116">Return value</span></span>

<span data-ttu-id="c3cee-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c3cee-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3cee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3cee-118">Remarks</span></span>

<span data-ttu-id="c3cee-119">Os aplicativos mais antigos (que negociaram a TAPI versão 1,3) recebem uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) ESPECIFICANDO LINEDEVSTATE \_ REINIT, o que exige que eles desliguem o uso da API e chamem [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) novamente para obter o novo número de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c3cee-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="c3cee-120">No entanto, ao contrário das versões anteriores da TAPI, essa versão não exige que todos os aplicativos sejam desligados antes de permitir que os aplicativos reinicialize; a reinicialização pode ocorrer imediatamente quando um novo dispositivo é criado (o desligamento completo ainda é necessário quando um provedor de serviços é removido do sistema).</span><span class="sxs-lookup"><span data-stu-id="c3cee-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="c3cee-121">Os aplicativos que dão suporte à TAPI versão 1,4 ou posterior são enviados uma mensagem de **\_ criação de linha** .</span><span class="sxs-lookup"><span data-stu-id="c3cee-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="c3cee-122">Isso informa a existência do novo dispositivo e seu novo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3cee-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="c3cee-123">Em seguida, o aplicativo pode escolher se deseja ou não tentar trabalhar com o novo dispositivo a seu lazer.</span><span class="sxs-lookup"><span data-stu-id="c3cee-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="c3cee-124">Essa mensagem é enviada a todos os aplicativos que dão suporte a esta ou a versões subsequentes da API que chamaram [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluindo aquelas que não têm dispositivos de linha abertos no momento.</span><span class="sxs-lookup"><span data-stu-id="c3cee-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cee-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3cee-125">Requirements</span></span>



| <span data-ttu-id="c3cee-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3cee-126">Requirement</span></span> | <span data-ttu-id="c3cee-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c3cee-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3cee-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c3cee-128">TAPI version</span></span><br/> | <span data-ttu-id="c3cee-129">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c3cee-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c3cee-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3cee-130">Header</span></span><br/>       | <dl> <span data-ttu-id="c3cee-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3cee-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cee-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3cee-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cee-133">**LINEDEVSTATE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="c3cee-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="c3cee-134">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="c3cee-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="c3cee-135">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="c3cee-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




