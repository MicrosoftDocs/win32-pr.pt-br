---
description: O \_ método get URL Obtém a URL.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'Método ITSdp:: get_Url (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759468"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="fbbab-103">Método de URL ITSdp:: get \_</span><span class="sxs-lookup"><span data-stu-id="fbbab-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="fbbab-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fbbab-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fbbab-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="fbbab-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fbbab-106">O método **Get \_ URL** Obtém a URL.</span><span class="sxs-lookup"><span data-stu-id="fbbab-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbbab-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="fbbab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbbab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbbab-109">*ppUrl* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fbbab-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbbab-110">Ponteiro para uma representação **BSTR** da URL.</span><span class="sxs-lookup"><span data-stu-id="fbbab-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbbab-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbbab-111">Return value</span></span>

<span data-ttu-id="fbbab-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="fbbab-112">This method can return one of these values.</span></span>



| <span data-ttu-id="fbbab-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fbbab-113">Return code</span></span>                                                                                   | <span data-ttu-id="fbbab-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbbab-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fbbab-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fbbab-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fbbab-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fbbab-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fbbab-118">O parâmetro *ppUrl* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="fbbab-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="fbbab-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fbbab-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="fbbab-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fbbab-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fbbab-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="fbbab-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fbbab-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fbbab-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="fbbab-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fbbab-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbbab-125">Remarks</span></span>

<span data-ttu-id="fbbab-126">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppUrl* .</span><span class="sxs-lookup"><span data-stu-id="fbbab-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="fbbab-127">Uma URL é normalmente usada para fazer referência a uma página da Web que contém recursos adicionais ou informações básicas sobre uma conferência.</span><span class="sxs-lookup"><span data-stu-id="fbbab-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbbab-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbbab-128">Requirements</span></span>



| <span data-ttu-id="fbbab-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbbab-129">Requirement</span></span> | <span data-ttu-id="fbbab-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fbbab-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbab-131">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="fbbab-131">TAPI version</span></span><br/> | <span data-ttu-id="fbbab-132">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fbbab-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fbbab-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbbab-133">Header</span></span><br/>       | <dl> <span data-ttu-id="fbbab-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbbab-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbbab-135">Library</span></span><br/>      | <dl> <span data-ttu-id="fbbab-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fbbab-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fbbab-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="fbbab-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbbab-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbbab-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbab-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="fbbab-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="fbbab-141">**ITSdp: URL de:p UT \_**</span><span class="sxs-lookup"><span data-stu-id="fbbab-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

