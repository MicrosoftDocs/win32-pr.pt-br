---
description: 'Método IEnumMedia:: clone – o método clone cria outro enumerador que contém o mesmo estado de enumeração que o atual.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'Método IEnumMedia:: clone (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114544"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="d6c6b-103">Método IEnumMedia:: clone</span><span class="sxs-lookup"><span data-stu-id="d6c6b-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="d6c6b-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d6c6b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d6c6b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d6c6b-106">O método **clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c6b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6c6b-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="d6c6b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6c6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c6b-109">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d6c6b-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c6b-110">Ponteiro para o novo objeto [**IEnumMedia**](ienummedia.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c6b-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c6b-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d6c6b-111">Return value</span></span>

<span data-ttu-id="d6c6b-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d6c6b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c6b-113">Value</span></span>                                                                                         | <span data-ttu-id="d6c6b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d6c6b-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d6c6b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d6c6b-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d6c6b-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d6c6b-118">O parâmetro *ppEnum* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="d6c6b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d6c6b-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d6c6b-121"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="d6c6b-122">Falha por motivos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="d6c6b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6c6b-123">Remarks</span></span>

<span data-ttu-id="d6c6b-124">A TAPI chama o método **AddRef** na interface [**IEnumMedia**](ienummedia.md) retornada por **IEnumMedia:: clone**.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="d6c6b-125">O aplicativo deve chamar **Release** na interface **IEnumMedia** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="d6c6b-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c6b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c6b-126">Requirements</span></span>



| <span data-ttu-id="d6c6b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c6b-127">Requirement</span></span> | <span data-ttu-id="d6c6b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c6b-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c6b-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d6c6b-129">TAPI version</span></span><br/> | <span data-ttu-id="d6c6b-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d6c6b-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d6c6b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6c6b-131">Header</span></span><br/>       | <dl> <span data-ttu-id="d6c6b-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6c6b-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6c6b-133">Library</span></span><br/>      | <dl> <span data-ttu-id="d6c6b-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d6c6b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c6b-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="d6c6b-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6b-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6c6b-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6c6b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c6b-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="d6c6b-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




