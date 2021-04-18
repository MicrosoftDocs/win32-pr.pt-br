---
description: O \_ método Get MediaTitle recupera um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Método ITMedia:: get_MediaTitle (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810136"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="56e23-105">Método ITMedia:: get \_ MediaTitle</span><span class="sxs-lookup"><span data-stu-id="56e23-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="56e23-106">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="56e23-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="56e23-107">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="56e23-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="56e23-108">O método **Get \_ MediaTitle** recupera um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição.</span><span class="sxs-lookup"><span data-stu-id="56e23-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="56e23-109">Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII.</span><span class="sxs-lookup"><span data-stu-id="56e23-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="56e23-110">Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="56e23-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e23-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56e23-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="56e23-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56e23-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e23-113">*ppMediaTitle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="56e23-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56e23-114">Ponteiro para um **BSTR** que contém o título da mídia.</span><span class="sxs-lookup"><span data-stu-id="56e23-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e23-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56e23-115">Return value</span></span>

<span data-ttu-id="56e23-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="56e23-116">This method can return one of these values.</span></span>



| <span data-ttu-id="56e23-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="56e23-117">Return code</span></span>                                                                                   | <span data-ttu-id="56e23-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="56e23-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="56e23-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="56e23-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="56e23-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="56e23-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="56e23-122">O parâmetro *ppMediaTitle* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="56e23-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="56e23-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="56e23-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="56e23-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="56e23-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="56e23-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="56e23-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="56e23-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="56e23-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="56e23-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="56e23-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="56e23-129">Remarks</span></span>

<span data-ttu-id="56e23-130">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppMediaTitle* .</span><span class="sxs-lookup"><span data-stu-id="56e23-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e23-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56e23-131">Requirements</span></span>



| <span data-ttu-id="56e23-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="56e23-132">Requirement</span></span> | <span data-ttu-id="56e23-133">Valor</span><span class="sxs-lookup"><span data-stu-id="56e23-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56e23-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="56e23-134">TAPI version</span></span><br/> | <span data-ttu-id="56e23-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="56e23-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="56e23-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56e23-136">Header</span></span><br/>       | <dl> <span data-ttu-id="56e23-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="56e23-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56e23-138">Library</span></span><br/>      | <dl> <span data-ttu-id="56e23-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="56e23-140">DLL</span><span class="sxs-lookup"><span data-stu-id="56e23-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="56e23-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e23-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="56e23-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e23-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="56e23-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="56e23-144">**ITMedia::P UT \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="56e23-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

