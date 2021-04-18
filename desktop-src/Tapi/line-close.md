---
description: A mensagem de fechamento de linha TAPI \_ é enviada quando o dispositivo de linha especificado é forçado a fechar. O identificador de dispositivo de linha ou qualquer identificador de chamada para chamadas na linha não será mais válido depois que essa mensagem for enviada.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Mensagem de LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788058"
---
# <a name="line_close-message"></a><span data-ttu-id="18808-104">Mensagem de fechamento de linha \_</span><span class="sxs-lookup"><span data-stu-id="18808-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="18808-105">A mensagem **de \_ fechamento de linha** TAPI é enviada quando o dispositivo de linha especificado é forçado a fechar.</span><span class="sxs-lookup"><span data-stu-id="18808-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="18808-106">O identificador de dispositivo de linha ou qualquer identificador de chamada para chamadas na linha não será mais válido depois que essa mensagem for enviada.</span><span class="sxs-lookup"><span data-stu-id="18808-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="18808-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18808-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18808-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="18808-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="18808-109">Um identificador para o dispositivo de linha que foi fechado.</span><span class="sxs-lookup"><span data-stu-id="18808-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="18808-110">Este identificador não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="18808-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="18808-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="18808-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="18808-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="18808-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="18808-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="18808-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="18808-114">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="18808-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="18808-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="18808-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="18808-116">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="18808-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="18808-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="18808-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="18808-118">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="18808-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18808-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18808-119">Return value</span></span>

<span data-ttu-id="18808-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="18808-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18808-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="18808-121">Remarks</span></span>

<span data-ttu-id="18808-122">A mensagem de **\_ fechamento de linha** é enviada para qualquer aplicativo somente após o provedor de serviços TAPI (TSP) ter fechado uma linha aberta de forma forçada.</span><span class="sxs-lookup"><span data-stu-id="18808-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="18808-123">Se a linha pode ou não ser reaberta imediatamente após um fechamento forçado ser específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18808-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="18808-124">A condição de causa pode ser uma alteração significativa do estado, um erro de hardware, uma perda de conexão com um servidor ou até mesmo impedir que um único aplicativo monopolizasse um dispositivo de linha por muito tempo.</span><span class="sxs-lookup"><span data-stu-id="18808-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="18808-125">Um dispositivo de linha também pode ser fechado à força após o usuário ter modificado a configuração dessa linha ou de seu driver.</span><span class="sxs-lookup"><span data-stu-id="18808-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="18808-126">Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em oposição à próxima reinicialização do sistema) e afetarem a exibição atual do dispositivo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá fechar o dispositivo de linha de forma forçada.</span><span class="sxs-lookup"><span data-stu-id="18808-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="18808-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18808-127">Requirements</span></span>



| <span data-ttu-id="18808-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="18808-128">Requirement</span></span> | <span data-ttu-id="18808-129">Valor</span><span class="sxs-lookup"><span data-stu-id="18808-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18808-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="18808-130">TAPI version</span></span><br/> | <span data-ttu-id="18808-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="18808-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="18808-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18808-132">Header</span></span><br/>       | <dl> <span data-ttu-id="18808-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="18808-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




