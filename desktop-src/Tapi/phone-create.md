---
description: A mensagem de \_ criação de telefone TAPI é enviada para informar os aplicativos sobre a criação de um novo dispositivo de telefone.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Mensagem de PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766966"
---
# <a name="phone_create-message"></a><span data-ttu-id="d639c-103">\_Criar mensagem de telefone</span><span class="sxs-lookup"><span data-stu-id="d639c-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="d639c-104">A mensagem **de \_ criação de telefone** TAPI é enviada para informar os aplicativos sobre a criação de um novo dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="d639c-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d639c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d639c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d639c-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="d639c-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="d639c-107">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d639c-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d639c-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="d639c-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d639c-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d639c-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d639c-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d639c-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d639c-111">O *hDeviceID* do dispositivo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="d639c-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="d639c-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d639c-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d639c-113">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d639c-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d639c-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d639c-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d639c-115">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d639c-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d639c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d639c-116">Return value</span></span>

<span data-ttu-id="d639c-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d639c-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d639c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d639c-118">Remarks</span></span>

<span data-ttu-id="d639c-119">Os aplicativos que negociaram a versão 1,3 da API recebem uma mensagem de [**\_ estado do telefone**](phone-state.md) que especifica o \_ REinicialização de PHONESTATE, o que exige que eles desliguem o uso da API e chamem [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) novamente para obter o novo número de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d639c-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="d639c-120">No entanto, a TAPI versão 1,4 e superior não exigem que todos os aplicativos sejam desligados antes de permitir que os aplicativos reinicialize; a reinicialização pode ocorrer imediatamente quando um novo dispositivo é criado.</span><span class="sxs-lookup"><span data-stu-id="d639c-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="d639c-121">Os aplicativos que dão suporte à TAPI versão 1,4 ou posterior são enviados para uma mensagem de **\_ criação de telefone** .</span><span class="sxs-lookup"><span data-stu-id="d639c-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="d639c-122">Isso informa a existência do novo dispositivo e seu novo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d639c-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="d639c-123">Em seguida, o aplicativo pode escolher se deseja ou não tentar trabalhar com o novo dispositivo a seu lazer.</span><span class="sxs-lookup"><span data-stu-id="d639c-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d639c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d639c-124">Requirements</span></span>



| <span data-ttu-id="d639c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d639c-125">Requirement</span></span> | <span data-ttu-id="d639c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d639c-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d639c-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d639c-127">TAPI version</span></span><br/> | <span data-ttu-id="d639c-128">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d639c-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d639c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d639c-129">Header</span></span><br/>       | <dl> <span data-ttu-id="d639c-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d639c-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d639c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d639c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d639c-132">**Estado do telefone \_**</span><span class="sxs-lookup"><span data-stu-id="d639c-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="d639c-133">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="d639c-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="d639c-134">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="d639c-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




