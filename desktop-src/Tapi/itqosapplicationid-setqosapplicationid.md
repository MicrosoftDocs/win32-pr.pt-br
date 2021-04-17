---
description: O método SetQOSApplicationID define o identificador de QOS para o aplicativo.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'Método ITQOSApplicationID:: SetQOSApplicationID (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753542"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="948c5-103">Método ITQOSApplicationID:: SetQOSApplicationID</span><span class="sxs-lookup"><span data-stu-id="948c5-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="948c5-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="948c5-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="948c5-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="948c5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="948c5-106">O método **SetQOSApplicationID** define o identificador de QoS para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="948c5-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="948c5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="948c5-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="948c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="948c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948c5-109">*pApplicationID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948c5-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948c5-110">Identificador exclusivo para o processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="948c5-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="948c5-111">*pApplicationGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948c5-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948c5-112">GUID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="948c5-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="948c5-113">*pSubIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948c5-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948c5-114">Sub-IDs associado à chamada atual.</span><span class="sxs-lookup"><span data-stu-id="948c5-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948c5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="948c5-115">Return value</span></span>

<span data-ttu-id="948c5-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="948c5-116">This method can return one of these values.</span></span>



| <span data-ttu-id="948c5-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="948c5-117">Return code</span></span>                                                                                   | <span data-ttu-id="948c5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="948c5-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="948c5-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="948c5-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="948c5-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="948c5-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="948c5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="948c5-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="948c5-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="948c5-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="948c5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948c5-123">Requirements</span></span>



| <span data-ttu-id="948c5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="948c5-124">Requirement</span></span> | <span data-ttu-id="948c5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="948c5-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="948c5-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="948c5-126">TAPI version</span></span><br/> | <span data-ttu-id="948c5-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="948c5-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="948c5-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="948c5-128">Header</span></span><br/>       | <dl> <span data-ttu-id="948c5-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="948c5-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="948c5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="948c5-130">Library</span></span><br/>      | <dl> <span data-ttu-id="948c5-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="948c5-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="948c5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="948c5-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="948c5-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948c5-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="948c5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="948c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948c5-135">**ITQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="948c5-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




