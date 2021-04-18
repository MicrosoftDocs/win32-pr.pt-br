---
title: Método de add_ConnectionStatusChanged IBasicDevice
description: Registra um manipulador de eventos para o evento ConnectionStatusChanged. | Método de add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API de streaming de mídia do método add_ConnectionStatusChanged
- API de streaming de mídia do método add_ConnectionStatusChanged, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781491"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="34609-107">Método IBasicDevice:: Add \_ ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="34609-107">IBasicDevice::add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="34609-108">Registra um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="34609-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="34609-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34609-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="34609-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34609-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34609-111">*manipulador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34609-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34609-112">Uma função de manipulador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="34609-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="34609-113">*token* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="34609-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="34609-114">Referência a um token que pode ser usado para cancelar o registro do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="34609-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34609-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34609-115">Return value</span></span>

<span data-ttu-id="34609-116">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="34609-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="34609-117">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="34609-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="34609-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="34609-118">Return code</span></span>                                                                          | <span data-ttu-id="34609-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="34609-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="34609-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34609-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="34609-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="34609-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34609-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="34609-122">Remarks</span></span>

<span data-ttu-id="34609-123">Para cancelar o registro do manipulador de eventos que foi registrado por esse método, passe o valor do *token* para o método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="34609-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="34609-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="34609-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34609-125">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="34609-125">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

