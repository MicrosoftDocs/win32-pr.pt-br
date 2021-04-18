---
description: A mensagem de DEVSPECIFIC de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: Mensagem de LINE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810461"
---
# <a name="line_devspecific-message"></a><span data-ttu-id="856c3-104">Mensagem de DEVSPECIFIC de linha \_</span><span class="sxs-lookup"><span data-stu-id="856c3-104">LINE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="856c3-105">A mensagem **de \_ DEVSPECIFIC de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada.</span><span class="sxs-lookup"><span data-stu-id="856c3-105">The TAPI **LINE\_DEVSPECIFIC** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="856c3-106">O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="856c3-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="856c3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="856c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856c3-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="856c3-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="856c3-109">Um identificador para um dispositivo de linha ou uma chamada.</span><span class="sxs-lookup"><span data-stu-id="856c3-109">A handle to either a line device or call.</span></span> <span data-ttu-id="856c3-110">Este é um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="856c3-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="856c3-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="856c3-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="856c3-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="856c3-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="856c3-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="856c3-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="856c3-114">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="856c3-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="856c3-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="856c3-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="856c3-116">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="856c3-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="856c3-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="856c3-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="856c3-118">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="856c3-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="856c3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="856c3-119">Return value</span></span>

<span data-ttu-id="856c3-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="856c3-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="856c3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="856c3-121">Remarks</span></span>

<span data-ttu-id="856c3-122">A **mensagem \_ DEVSPECIFIC de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="856c3-122">The **LINE\_DEVSPECIFIC** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="856c3-123">Seu significado é específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="856c3-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="856c3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="856c3-124">Requirements</span></span>



| <span data-ttu-id="856c3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="856c3-125">Requirement</span></span> | <span data-ttu-id="856c3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="856c3-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="856c3-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="856c3-127">TAPI version</span></span><br/> | <span data-ttu-id="856c3-128">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="856c3-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="856c3-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="856c3-129">Header</span></span><br/>       | <dl> <span data-ttu-id="856c3-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="856c3-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




