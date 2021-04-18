---
description: O \_ loop Put define o modo de loopback multicast.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'IMulticastControl: método de ut_LoopbackMode de:p (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810142"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="33602-103">IMulticastControl::p \_ método UT loopbackmode</span><span class="sxs-lookup"><span data-stu-id="33602-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="33602-104">\[**Put \_ Loopbackmode** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="33602-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="33602-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="33602-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="33602-106">O **\_ loop Put** define o modo de loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="33602-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="33602-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33602-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="33602-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33602-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33602-109">*modo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33602-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33602-110">[**Multicast \_ Descritor de \_ modo loopback**](multicast-loopback-mode.md) do novo modo de loopback.</span><span class="sxs-lookup"><span data-stu-id="33602-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33602-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33602-111">Return value</span></span>

<span data-ttu-id="33602-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="33602-112">This method can return one of these values.</span></span>



| <span data-ttu-id="33602-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="33602-113">Return code</span></span>                                                                                  | <span data-ttu-id="33602-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="33602-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="33602-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33602-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="33602-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="33602-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="33602-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="33602-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="33602-118">O parâmetro de *modo* não é válido.</span><span class="sxs-lookup"><span data-stu-id="33602-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="33602-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33602-119">Requirements</span></span>



| <span data-ttu-id="33602-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33602-120">Requirement</span></span> | <span data-ttu-id="33602-121">Valor</span><span class="sxs-lookup"><span data-stu-id="33602-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33602-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="33602-122">TAPI version</span></span><br/> | <span data-ttu-id="33602-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="33602-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="33602-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33602-124">Header</span></span><br/>       | <dl> <span data-ttu-id="33602-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="33602-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="33602-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33602-126">Library</span></span><br/>      | <dl> <span data-ttu-id="33602-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33602-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="33602-128">DLL</span><span class="sxs-lookup"><span data-stu-id="33602-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="33602-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33602-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="33602-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="33602-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33602-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="33602-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




