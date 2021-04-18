---
description: A mensagem de DEVSPECIFICEX de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Mensagem de LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780596"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="18b3a-104">Mensagem de DEVSPECIFICEX de linha \_</span><span class="sxs-lookup"><span data-stu-id="18b3a-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="18b3a-105">A mensagem **de \_ DEVSPECIFICEX de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada.</span><span class="sxs-lookup"><span data-stu-id="18b3a-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="18b3a-106">O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3a-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="18b3a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18b3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b3a-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="18b3a-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="18b3a-109">Um identificador para um dispositivo de linha ou uma chamada.</span><span class="sxs-lookup"><span data-stu-id="18b3a-109">A handle to either a line device or call.</span></span> <span data-ttu-id="18b3a-110">Esse parâmetro é específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3a-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="18b3a-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="18b3a-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="18b3a-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="18b3a-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="18b3a-114">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3a-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="18b3a-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="18b3a-116">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3a-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="18b3a-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="18b3a-118">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3a-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b3a-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18b3a-119">Return value</span></span>

<span data-ttu-id="18b3a-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="18b3a-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b3a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="18b3a-121">Remarks</span></span>

<span data-ttu-id="18b3a-122">A **mensagem \_ DEVSPECIFICEX de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="18b3a-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="18b3a-123">Seu significado é específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3a-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b3a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18b3a-124">Requirements</span></span>



| <span data-ttu-id="18b3a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b3a-125">Requirement</span></span> | <span data-ttu-id="18b3a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="18b3a-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18b3a-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="18b3a-127">TAPI version</span></span><br/> | <span data-ttu-id="18b3a-128">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="18b3a-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="18b3a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18b3a-129">Header</span></span><br/>       | <dl> <span data-ttu-id="18b3a-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="18b3a-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




