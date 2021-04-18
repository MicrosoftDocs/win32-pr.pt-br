---
description: O \_ método Get CharacterSet Obtém um \_ \_ descritor de conjunto de caracteres de blob do conjunto de caracteres usado no blob de conferência atual.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Método ITConferenceBlob:: get_CharacterSet (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810138"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="cc6c4-103">Método ITConferenceBlob:: get \_ CharacterSet</span><span class="sxs-lookup"><span data-stu-id="cc6c4-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="cc6c4-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cc6c4-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cc6c4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cc6c4-106">O método **Get \_ CharacterSet** Obtém um descritor de [**\_ \_ conjunto de caracteres de blob**](blob-character-set.md) do conjunto de caracteres usado no blob de conferência atual.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc6c4-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="cc6c4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc6c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc6c4-109">*pCharacterSet* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc6c4-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6c4-110">Ponteiro para um descritor de [**\_ \_ conjunto de caracteres de blob**](blob-character-set.md) do conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc6c4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc6c4-111">Return value</span></span>

<span data-ttu-id="cc6c4-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cc6c4-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc6c4-113">Return code</span></span>                                                                                                   | <span data-ttu-id="cc6c4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc6c4-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc6c4-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="cc6c4-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="cc6c4-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="cc6c4-118">O parâmetro *pCharacterSet* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="cc6c4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="cc6c4-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="cc6c4-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="cc6c4-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cc6c4-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="cc6c4-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="cc6c4-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="cc6c4-126">*pCharacterSet* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="cc6c4-127"><dt>**RESULTADO ERRO de \_ dados inválidos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="cc6c4-128">O conjunto de caracteres atual é inválido ou não está disponível.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="cc6c4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc6c4-129">Requirements</span></span>



| <span data-ttu-id="cc6c4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc6c4-130">Requirement</span></span> | <span data-ttu-id="cc6c4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="cc6c4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6c4-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cc6c4-132">TAPI version</span></span><br/> | <span data-ttu-id="cc6c4-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cc6c4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cc6c4-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc6c4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="cc6c4-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc6c4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc6c4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="cc6c4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cc6c4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cc6c4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="cc6c4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc6c4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc6c4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc6c4-141">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="cc6c4-142">**\_conjunto de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




