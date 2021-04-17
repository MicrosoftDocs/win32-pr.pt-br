---
description: O método ReOrderCapabilities define um novo pedido para recursos de formato.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Método ITFormatControl:: ReOrderCapabilities (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759470"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="a2299-103">Método ITFormatControl:: ReOrderCapabilities</span><span class="sxs-lookup"><span data-stu-id="a2299-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="a2299-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a2299-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a2299-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a2299-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a2299-106">O método **ReOrderCapabilities** define um novo pedido para recursos de formato.</span><span class="sxs-lookup"><span data-stu-id="a2299-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2299-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2299-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="a2299-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2299-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2299-109">*pdwIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2299-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2299-110">Índice do formato que está sendo reordenado.</span><span class="sxs-lookup"><span data-stu-id="a2299-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="a2299-111">*pfEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2299-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2299-112">Indica se o formato deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a2299-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a2299-113">*pfPublicize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2299-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2299-114">Indica se o formato deve ser disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="a2299-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="a2299-115">*dwNumIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2299-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2299-116">Novo número de índice para o formato.</span><span class="sxs-lookup"><span data-stu-id="a2299-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2299-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2299-117">Return value</span></span>

<span data-ttu-id="a2299-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a2299-118">This method can return one of these values.</span></span>



| <span data-ttu-id="a2299-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a2299-119">Return code</span></span>                                                                                   | <span data-ttu-id="a2299-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2299-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a2299-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a2299-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a2299-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a2299-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a2299-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a2299-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a2299-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a2299-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2299-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2299-125">Remarks</span></span>

<span data-ttu-id="a2299-126">O método [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) deve ser chamado antes do uso desse método.</span><span class="sxs-lookup"><span data-stu-id="a2299-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2299-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2299-127">Requirements</span></span>



| <span data-ttu-id="a2299-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2299-128">Requirement</span></span> | <span data-ttu-id="a2299-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a2299-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2299-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a2299-130">TAPI version</span></span><br/> | <span data-ttu-id="a2299-131">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a2299-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="a2299-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2299-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a2299-133"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2299-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2299-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2299-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a2299-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2299-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="a2299-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a2299-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a2299-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2299-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2299-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2299-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2299-139">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="a2299-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="a2299-140">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a2299-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




