---
description: 'Método IEnumTime:: Skip – o método Skip ignora o próximo número especificado de elementos na sequência de enumeração.'
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'Método IEnumTime:: Skip (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190a98c14cb8f551276a173e2d73872d876f2ceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090714"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="d3979-103">Método IEnumTime:: Skip</span><span class="sxs-lookup"><span data-stu-id="d3979-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="d3979-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d3979-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d3979-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d3979-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d3979-106">O método **Skip** ignora o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="d3979-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3979-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3979-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="d3979-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3979-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3979-109">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3979-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3979-110">Número de elementos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="d3979-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3979-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d3979-111">Return value</span></span>

<span data-ttu-id="d3979-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d3979-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d3979-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d3979-113">Return code</span></span>                                                                             | <span data-ttu-id="d3979-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3979-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="d3979-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d3979-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d3979-116">O número de elementos ignorados foi *celt*.</span><span class="sxs-lookup"><span data-stu-id="d3979-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="d3979-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="d3979-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d3979-118">O número de elementos ignorados não era *celt*.</span><span class="sxs-lookup"><span data-stu-id="d3979-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d3979-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3979-119">Requirements</span></span>



| <span data-ttu-id="d3979-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3979-120">Requirement</span></span> | <span data-ttu-id="d3979-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d3979-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3979-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d3979-122">TAPI version</span></span><br/> | <span data-ttu-id="d3979-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d3979-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d3979-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3979-124">Header</span></span><br/>       | <dl> <span data-ttu-id="d3979-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3979-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3979-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3979-126">Library</span></span><br/>      | <dl> <span data-ttu-id="d3979-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3979-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d3979-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d3979-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="d3979-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3979-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3979-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d3979-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3979-131">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="d3979-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




