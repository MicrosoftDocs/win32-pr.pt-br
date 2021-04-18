---
title: Método de BasicDevice.add_ConnectionStatusChanged
description: Registra um manipulador de eventos para o evento ConnectionStatusChanged. | Método de BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API de streaming de mídia do método add_ConnectionStatusChanged
- API de streaming de mídia do método add_ConnectionStatusChanged, interface BasicDevice
- API de streaming de mídia da interface BasicDevice, método add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105814037"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="a99eb-107">BasicDevice. Adicione o \_ método ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="a99eb-107">BasicDevice.add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="a99eb-108">Registra um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a99eb-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99eb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a99eb-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="a99eb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a99eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a99eb-111">*manipulador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a99eb-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a99eb-112">Uma função de manipulador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a99eb-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="a99eb-113">*token* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a99eb-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a99eb-114">Referência a um token que pode ser usado para cancelar o registro do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="a99eb-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a99eb-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a99eb-115">Return value</span></span>

<span data-ttu-id="a99eb-116">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a99eb-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a99eb-117">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a99eb-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a99eb-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a99eb-118">Return code</span></span>                                                                          | <span data-ttu-id="a99eb-119">Description</span><span class="sxs-lookup"><span data-stu-id="a99eb-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a99eb-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a99eb-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a99eb-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a99eb-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a99eb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a99eb-122">Remarks</span></span>

<span data-ttu-id="a99eb-123">Para cancelar o registro do manipulador de eventos que foi registrado por esse método, passe o valor do *token* para o método [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a99eb-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="a99eb-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a99eb-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a99eb-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a99eb-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

