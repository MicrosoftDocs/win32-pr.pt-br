---
description: O método GetCurrentFormat recupera o formato de mídia do fluxo atual.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Método ITFormatControl:: GetCurrentFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761962"
---
# <a name="itformatcontrolgetcurrentformat-method"></a><span data-ttu-id="0c173-103">Método ITFormatControl:: GetCurrentFormat</span><span class="sxs-lookup"><span data-stu-id="0c173-103">ITFormatControl::GetCurrentFormat method</span></span>

<span data-ttu-id="0c173-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0c173-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c173-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="0c173-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0c173-106">O método **GetCurrentFormat** recupera o formato de mídia do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="0c173-106">The **GetCurrentFormat** method retrieves the media format of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c173-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c173-107">Syntax</span></span>


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="0c173-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c173-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c173-109">*ppMediaType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c173-109">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c173-110">Ponteiro para um descritor de **\_ \_ tipo de mídia am** do formato de terminal.</span><span class="sxs-lookup"><span data-stu-id="0c173-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="0c173-111">Para obter mais informações sobre o **\_ \_ tipo de mídia am**, consulte a documentação do DirectX.</span><span class="sxs-lookup"><span data-stu-id="0c173-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c173-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c173-112">Return value</span></span>

<span data-ttu-id="0c173-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0c173-113">This method can return one of these values.</span></span>



| <span data-ttu-id="0c173-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c173-114">Return code</span></span>                                                                                   | <span data-ttu-id="0c173-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c173-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0c173-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c173-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0c173-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0c173-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0c173-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0c173-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0c173-119">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0c173-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0c173-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c173-120">Requirements</span></span>



| <span data-ttu-id="0c173-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c173-121">Requirement</span></span> | <span data-ttu-id="0c173-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0c173-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c173-123">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="0c173-123">TAPI version</span></span><br/> | <span data-ttu-id="0c173-124">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="0c173-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="0c173-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c173-125">Header</span></span><br/>       | <dl> <span data-ttu-id="0c173-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c173-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c173-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c173-127">Library</span></span><br/>      | <dl> <span data-ttu-id="0c173-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c173-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="0c173-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0c173-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="0c173-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c173-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c173-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c173-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c173-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="0c173-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




