---
description: O \_ método Get loopbackmode Obtém o modo de loopback multicast.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Método IMulticastControl:: get_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761965"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="4b732-103">Método testloopbackmode de IMulticastControl:: get \_</span><span class="sxs-lookup"><span data-stu-id="4b732-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="4b732-104">\[**obter \_ Loopbackmode** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4b732-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b732-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4b732-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4b732-106">O método **Get \_ loopbackmode** Obtém o modo de loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="4b732-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b732-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b732-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="4b732-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b732-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b732-109">*pMode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4b732-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b732-110">Ponteiro para o descritor do [**\_ \_ modo de loopback multicast**](multicast-loopback-mode.md) do modo de loopback atual.</span><span class="sxs-lookup"><span data-stu-id="4b732-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b732-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b732-111">Return value</span></span>

<span data-ttu-id="4b732-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4b732-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4b732-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4b732-113">Value</span></span>                                                                                        | <span data-ttu-id="4b732-114">Significado</span><span class="sxs-lookup"><span data-stu-id="4b732-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4b732-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b732-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4b732-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4b732-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="4b732-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4b732-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4b732-118">O parâmetro *pMode* não é válido.</span><span class="sxs-lookup"><span data-stu-id="4b732-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b732-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b732-119">Requirements</span></span>



| <span data-ttu-id="4b732-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b732-120">Requirement</span></span> | <span data-ttu-id="4b732-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4b732-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b732-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4b732-122">TAPI version</span></span><br/> | <span data-ttu-id="4b732-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4b732-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4b732-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b732-124">Header</span></span><br/>       | <dl> <span data-ttu-id="4b732-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b732-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="4b732-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b732-126">Library</span></span><br/>      | <dl> <span data-ttu-id="4b732-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b732-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4b732-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4b732-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="4b732-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b732-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4b732-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b732-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b732-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="4b732-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




