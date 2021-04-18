---
description: O \_ método Get Description obtém a descrição da sessão (BSTR).
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'Método ITSdp:: get_Description (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810134"
---
# <a name="itsdpget_description-method"></a><span data-ttu-id="fa974-103">Método de descrição de ITSdp:: get \_</span><span class="sxs-lookup"><span data-stu-id="fa974-103">ITSdp::get\_Description method</span></span>

<span data-ttu-id="fa974-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fa974-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fa974-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="fa974-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fa974-106">O método **Get \_ Description** Obtém a descrição da sessão (**BSTR**).</span><span class="sxs-lookup"><span data-stu-id="fa974-106">The **get\_Description** method gets the session description (**BSTR**).</span></span> <span data-ttu-id="fa974-107">Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII.</span><span class="sxs-lookup"><span data-stu-id="fa974-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="fa974-108">(Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .)</span><span class="sxs-lookup"><span data-stu-id="fa974-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa974-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa974-109">Syntax</span></span>


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a><span data-ttu-id="fa974-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa974-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa974-111">*ppDescription* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa974-111">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa974-112">Ponteiro para um **BSTR** que contém a descrição da sessão.</span><span class="sxs-lookup"><span data-stu-id="fa974-112">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa974-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa974-113">Return value</span></span>

<span data-ttu-id="fa974-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="fa974-114">This method can return one of these values.</span></span>



| <span data-ttu-id="fa974-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa974-115">Return code</span></span>                                                                                   | <span data-ttu-id="fa974-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa974-116">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa974-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fa974-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa974-118">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="fa974-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fa974-120">O parâmetro *ppDescription* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="fa974-120">The *ppDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="fa974-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fa974-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="fa974-122">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="fa974-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fa974-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="fa974-124">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fa974-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fa974-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="fa974-126">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="fa974-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa974-127">Remarks</span></span>

<span data-ttu-id="fa974-128">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar o parâmetro *ppDescription* .</span><span class="sxs-lookup"><span data-stu-id="fa974-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the *ppDescription* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa974-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa974-129">Requirements</span></span>



| <span data-ttu-id="fa974-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa974-130">Requirement</span></span> | <span data-ttu-id="fa974-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fa974-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa974-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="fa974-132">TAPI version</span></span><br/> | <span data-ttu-id="fa974-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fa974-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fa974-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa974-134">Header</span></span><br/>       | <dl> <span data-ttu-id="fa974-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa974-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa974-136">Library</span></span><br/>      | <dl> <span data-ttu-id="fa974-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fa974-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fa974-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="fa974-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa974-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa974-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa974-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa974-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="fa974-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="fa974-142">**Descrição do ITSdp::p UT \_**</span><span class="sxs-lookup"><span data-stu-id="fa974-142">**ITSdp::put\_Description**</span></span>](itsdp-put-description.md)
</dt> </dl>

 

