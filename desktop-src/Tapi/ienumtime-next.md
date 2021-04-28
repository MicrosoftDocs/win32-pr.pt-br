---
description: 'Método IEnumTime:: Next – o próximo método obtém o próximo número especificado de elementos na sequência de enumeração.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'Método IEnumTime:: Next (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118384"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="a5033-103">Método IEnumTime:: Next</span><span class="sxs-lookup"><span data-stu-id="a5033-103">IEnumTime::Next method</span></span>

<span data-ttu-id="a5033-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a5033-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a5033-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a5033-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a5033-106">O **próximo** método obtém o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="a5033-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5033-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5033-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="a5033-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5033-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5033-109">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5033-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5033-110">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="a5033-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-111">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5033-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5033-112">Ponteiro para a interface [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="a5033-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-113">*pceltFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5033-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5033-114">Aponta para o número de elementos realmente fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a5033-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="a5033-115">Poderá ser **NULL** se *celt* for 1.</span><span class="sxs-lookup"><span data-stu-id="a5033-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5033-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a5033-116">Return value</span></span>

<span data-ttu-id="a5033-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a5033-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a5033-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a5033-118">Value</span></span>                                                                                     | <span data-ttu-id="a5033-119">Significado</span><span class="sxs-lookup"><span data-stu-id="a5033-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="a5033-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="a5033-121">O método retornou *celt* número de elementos.</span><span class="sxs-lookup"><span data-stu-id="a5033-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="a5033-122"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="a5033-123">O número de elementos restantes era menor que *celt*.</span><span class="sxs-lookup"><span data-stu-id="a5033-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="a5033-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="a5033-125">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="a5033-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="a5033-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5033-126">Remarks</span></span>

<span data-ttu-id="a5033-127">A TAPI chama o método **AddRef** na interface [**ITTime**](ittime.md) retornada por **IEnumTime:: Next**.</span><span class="sxs-lookup"><span data-stu-id="a5033-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="a5033-128">O aplicativo deve chamar **Release** na interface **ITTime** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="a5033-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5033-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5033-129">Requirements</span></span>



| <span data-ttu-id="a5033-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5033-130">Requirement</span></span> | <span data-ttu-id="a5033-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a5033-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5033-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a5033-132">TAPI version</span></span><br/> | <span data-ttu-id="a5033-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a5033-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a5033-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5033-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a5033-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5033-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5033-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a5033-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a5033-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a5033-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a5033-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5033-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a5033-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5033-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="a5033-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




