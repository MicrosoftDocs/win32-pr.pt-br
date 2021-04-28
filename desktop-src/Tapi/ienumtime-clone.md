---
description: 'Método IEnumTime:: clone – o método clone cria outro enumerador que contém o mesmo estado de enumeração que o atual.'
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Método IEnumTime:: clone (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406dac1fad611ee5d3cb6c8b6ef32dfdb62cc963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090734"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="38302-103">Método IEnumTime:: clone</span><span class="sxs-lookup"><span data-stu-id="38302-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="38302-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="38302-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="38302-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="38302-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="38302-106">O método **clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual.</span><span class="sxs-lookup"><span data-stu-id="38302-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="38302-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38302-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="38302-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38302-109">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38302-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38302-110">Ponteiro para o novo objeto [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="38302-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38302-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="38302-111">Return value</span></span>

<span data-ttu-id="38302-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="38302-112">This method can return one of these values.</span></span>



| <span data-ttu-id="38302-113">Valor</span><span class="sxs-lookup"><span data-stu-id="38302-113">Value</span></span>                                                                                         | <span data-ttu-id="38302-114">Significado</span><span class="sxs-lookup"><span data-stu-id="38302-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="38302-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38302-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="38302-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="38302-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="38302-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="38302-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="38302-118">O parâmetro *ppEnum* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="38302-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="38302-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="38302-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="38302-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="38302-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="38302-121"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="38302-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="38302-122">Falha por motivos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="38302-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="38302-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="38302-123">Remarks</span></span>

<span data-ttu-id="38302-124">A TAPI chama o método **AddRef** na interface [**IEnumTime**](ienumtime.md) retornada por **IEnumTime:: clone**.</span><span class="sxs-lookup"><span data-stu-id="38302-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="38302-125">O aplicativo deve chamar **Release** na interface **IEnumTime** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="38302-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="38302-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38302-126">Requirements</span></span>



| <span data-ttu-id="38302-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="38302-127">Requirement</span></span> | <span data-ttu-id="38302-128">Valor</span><span class="sxs-lookup"><span data-stu-id="38302-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38302-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="38302-129">TAPI version</span></span><br/> | <span data-ttu-id="38302-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="38302-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="38302-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38302-131">Header</span></span><br/>       | <dl> <span data-ttu-id="38302-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="38302-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="38302-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38302-133">Library</span></span><br/>      | <dl> <span data-ttu-id="38302-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38302-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="38302-135">DLL</span><span class="sxs-lookup"><span data-stu-id="38302-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="38302-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38302-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38302-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="38302-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38302-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="38302-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




