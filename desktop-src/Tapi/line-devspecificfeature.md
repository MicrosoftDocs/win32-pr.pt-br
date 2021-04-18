---
description: A mensagem de DEVSPECIFICFEATURE de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Mensagem de LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788057"
---
# <a name="line_devspecificfeature-message"></a><span data-ttu-id="92bb2-104">Mensagem de DEVSPECIFICFEATURE de linha \_</span><span class="sxs-lookup"><span data-stu-id="92bb2-104">LINE\_DEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="92bb2-105">A mensagem **de \_ DEVSPECIFICFEATURE de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada.</span><span class="sxs-lookup"><span data-stu-id="92bb2-105">The TAPI **LINE\_DEVSPECIFICFEATURE** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="92bb2-106">O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92bb2-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="92bb2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92bb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bb2-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="92bb2-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="92bb2-109">Um identificador para um dispositivo de linha ou uma chamada.</span><span class="sxs-lookup"><span data-stu-id="92bb2-109">A handle to either a line device or call.</span></span> <span data-ttu-id="92bb2-110">Este é um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="92bb2-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="92bb2-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="92bb2-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="92bb2-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="92bb2-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="92bb2-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="92bb2-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="92bb2-114">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92bb2-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="92bb2-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="92bb2-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="92bb2-116">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92bb2-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="92bb2-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="92bb2-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="92bb2-118">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92bb2-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bb2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92bb2-119">Return value</span></span>

<span data-ttu-id="92bb2-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="92bb2-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92bb2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="92bb2-121">Remarks</span></span>

<span data-ttu-id="92bb2-122">A **mensagem \_ DEVSPECIFICFEATURE de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="92bb2-122">The **LINE\_DEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) function.</span></span> <span data-ttu-id="92bb2-123">Seu significado é específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92bb2-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="92bb2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bb2-124">Requirements</span></span>



| <span data-ttu-id="92bb2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92bb2-125">Requirement</span></span> | <span data-ttu-id="92bb2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="92bb2-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92bb2-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="92bb2-127">TAPI version</span></span><br/> | <span data-ttu-id="92bb2-128">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="92bb2-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="92bb2-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92bb2-129">Header</span></span><br/>       | <dl> <span data-ttu-id="92bb2-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="92bb2-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




