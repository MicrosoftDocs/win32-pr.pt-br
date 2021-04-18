---
description: A mensagem de fechamento de telefone TAPI \_ é enviada quando um dispositivo de telefone aberto é forçado a ser fechado como parte da reclamação de recurso. O identificador do dispositivo não será mais válido depois que essa mensagem for enviada.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Mensagem de PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810126"
---
# <a name="phone_close-message"></a><span data-ttu-id="df062-104">Mensagem de fechamento do telefone \_</span><span class="sxs-lookup"><span data-stu-id="df062-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="df062-105">A mensagem **de \_ fechamento de telefone** TAPI é enviada quando um dispositivo de telefone aberto é forçado a ser fechado como parte da reclamação de recurso.</span><span class="sxs-lookup"><span data-stu-id="df062-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="df062-106">O identificador do dispositivo não será mais válido depois que essa mensagem for enviada.</span><span class="sxs-lookup"><span data-stu-id="df062-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="df062-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df062-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df062-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="df062-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="df062-109">Um identificador para o dispositivo de telefone aberto que foi fechado.</span><span class="sxs-lookup"><span data-stu-id="df062-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="df062-110">O identificador não é mais válido depois que esta mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="df062-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="df062-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="df062-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="df062-112">A instância de retorno de chamada do aplicativo que forneceu ao abrir o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="df062-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="df062-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="df062-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="df062-114">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="df062-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="df062-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="df062-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="df062-116">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="df062-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="df062-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="df062-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="df062-118">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="df062-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df062-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df062-119">Return value</span></span>

<span data-ttu-id="df062-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="df062-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df062-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="df062-121">Remarks</span></span>

<span data-ttu-id="df062-122">A mensagem de **\_ fechamento do telefone** é enviada somente a um aplicativo depois que um telefone aberto é forçado a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="df062-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="df062-123">Isso pode ser feito para impedir que um único aplicativo monopolizasse um dispositivo de telefone por muito tempo.</span><span class="sxs-lookup"><span data-stu-id="df062-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="df062-124">Se o telefone pode ser reaberto imediatamente após um fechamento forçado é específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df062-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="df062-125">Um dispositivo de telefone aberto também pode ser fechado à força após o usuário ter modificado a configuração desse telefone ou de seu driver.</span><span class="sxs-lookup"><span data-stu-id="df062-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="df062-126">Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em vez de após a próxima reinicialização do sistema) e essas alterações afetarem a exibição atual do dispositivo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá forçar o fechamento do dispositivo telefônico.</span><span class="sxs-lookup"><span data-stu-id="df062-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="df062-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df062-127">Requirements</span></span>



| <span data-ttu-id="df062-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="df062-128">Requirement</span></span> | <span data-ttu-id="df062-129">Valor</span><span class="sxs-lookup"><span data-stu-id="df062-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="df062-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="df062-130">TAPI version</span></span><br/> | <span data-ttu-id="df062-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="df062-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="df062-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df062-132">Header</span></span><br/>       | <dl> <span data-ttu-id="df062-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="df062-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




