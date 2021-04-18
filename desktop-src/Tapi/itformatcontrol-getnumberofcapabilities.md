---
description: O método GetNumberOfCapabilities recupera o número de recursos associados ao formato atual.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'Método ITFormatControl:: GetNumberOfCapabilities (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767756"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="cd649-103">Método ITFormatControl:: GetNumberOfCapabilities</span><span class="sxs-lookup"><span data-stu-id="cd649-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="cd649-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cd649-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd649-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cd649-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cd649-106">O método **GetNumberOfCapabilities** recupera o número de recursos associados ao formato atual.</span><span class="sxs-lookup"><span data-stu-id="cd649-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd649-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd649-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="cd649-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd649-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd649-109">*pdwCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd649-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd649-110">Contagem dos recursos.</span><span class="sxs-lookup"><span data-stu-id="cd649-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd649-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd649-111">Return value</span></span>

<span data-ttu-id="cd649-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cd649-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cd649-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cd649-113">Return code</span></span>                                                                                   | <span data-ttu-id="cd649-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd649-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cd649-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd649-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cd649-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cd649-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cd649-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cd649-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cd649-118">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="cd649-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cd649-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd649-119">Requirements</span></span>



| <span data-ttu-id="cd649-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd649-120">Requirement</span></span> | <span data-ttu-id="cd649-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cd649-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd649-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cd649-122">TAPI version</span></span><br/> | <span data-ttu-id="cd649-123">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="cd649-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="cd649-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd649-124">Header</span></span><br/>       | <dl> <span data-ttu-id="cd649-125"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd649-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd649-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd649-126">Library</span></span><br/>      | <dl> <span data-ttu-id="cd649-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd649-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="cd649-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cd649-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="cd649-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd649-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd649-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd649-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd649-131">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="cd649-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




