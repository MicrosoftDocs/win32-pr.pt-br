---
description: A mensagem de CALLHUBCLOSE de linha TAPI \_ é enviada quando um hub de chamada é fechado.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Mensagem de LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757208"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="4605a-103">Mensagem de CALLHUBCLOSE de linha \_</span><span class="sxs-lookup"><span data-stu-id="4605a-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="4605a-104">A mensagem **de \_ CALLHUBCLOSE de linha** TAPI é enviada quando um hub de chamada é fechado.</span><span class="sxs-lookup"><span data-stu-id="4605a-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4605a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4605a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4605a-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="4605a-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4605a-107">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="4605a-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="4605a-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="4605a-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4605a-109">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="4605a-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="4605a-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4605a-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4605a-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4605a-111">Reserved.</span></span> <span data-ttu-id="4605a-112">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="4605a-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4605a-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4605a-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4605a-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4605a-114">Reserved.</span></span> <span data-ttu-id="4605a-115">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="4605a-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4605a-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4605a-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4605a-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4605a-117">Reserved.</span></span> <span data-ttu-id="4605a-118">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="4605a-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4605a-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4605a-119">Return value</span></span>

<span data-ttu-id="4605a-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4605a-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4605a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4605a-121">Remarks</span></span>

<span data-ttu-id="4605a-122">Essa mensagem é originada com TAPI em vez de com um provedor de serviços, portanto, não há nenhuma mensagem TSPI correspondente.</span><span class="sxs-lookup"><span data-stu-id="4605a-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4605a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4605a-123">Requirements</span></span>



| <span data-ttu-id="4605a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4605a-124">Requirement</span></span> | <span data-ttu-id="4605a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4605a-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4605a-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4605a-126">TAPI version</span></span><br/> | <span data-ttu-id="4605a-127">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="4605a-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4605a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4605a-128">Header</span></span><br/>       | <dl> <span data-ttu-id="4605a-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4605a-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




