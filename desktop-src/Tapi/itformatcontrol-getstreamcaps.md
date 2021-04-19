---
description: O método GetStreamCaps recupera os recursos associados a um determinado índice de formato.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Método ITFormatControl:: GetStreamCaps (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782912"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="6f4ce-103">Método ITFormatControl:: GetStreamCaps</span><span class="sxs-lookup"><span data-stu-id="6f4ce-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="6f4ce-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6f4ce-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6f4ce-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6f4ce-106">O método **GetStreamCaps** recupera os recursos associados a um determinado índice de formato.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4ce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f4ce-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="6f4ce-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f4ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f4ce-109">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6f4ce-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4ce-110">Índice do formato que está sendo investigado.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="6f4ce-111">*ppMediaType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f4ce-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4ce-112">Ponteiro para um descritor de **\_ \_ tipo de mídia am** do formato de terminal.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="6f4ce-113">Para obter mais informações sobre o **\_ \_ tipo de mídia am**, consulte a documentação do DirectX.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="6f4ce-114">*pStreamConfigCaps* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f4ce-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4ce-115">Uma [**estrutura \_ \_ \_ Caps de configuração de fluxo TAPI**](tapi-stream-config-caps.md) que fornece informações detalhadas sobre os recursos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="6f4ce-116">*pfEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f4ce-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4ce-117">Indica se o formato associado ao índice atual está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f4ce-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f4ce-118">Return value</span></span>

<span data-ttu-id="6f4ce-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-119">This method can return one of these values.</span></span>



| <span data-ttu-id="6f4ce-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6f4ce-120">Return code</span></span>                                                                                   | <span data-ttu-id="6f4ce-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f4ce-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6f4ce-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ce-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6f4ce-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6f4ce-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ce-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6f4ce-125">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="6f4ce-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f4ce-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f4ce-126">Requirements</span></span>



| <span data-ttu-id="6f4ce-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4ce-127">Requirement</span></span> | <span data-ttu-id="6f4ce-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6f4ce-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4ce-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6f4ce-129">TAPI version</span></span><br/> | <span data-ttu-id="6f4ce-130">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6f4ce-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="6f4ce-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f4ce-131">Header</span></span><br/>       | <dl> <span data-ttu-id="6f4ce-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ce-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f4ce-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f4ce-133">Library</span></span><br/>      | <dl> <span data-ttu-id="6f4ce-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ce-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="6f4ce-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4ce-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="6f4ce-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ce-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4ce-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f4ce-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4ce-138">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="6f4ce-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f4ce-139">**\_limites de \_ configuração de fluxo TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="6f4ce-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




