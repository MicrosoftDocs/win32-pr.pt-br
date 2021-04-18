---
description: O \_ método Put URL define a URL.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: 'ITSdp: método de ut_Url de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769414"
---
# <a name="itsdpput_url-method"></a><span data-ttu-id="b08d9-103">ITSdp: método de URL de:p UT \_</span><span class="sxs-lookup"><span data-stu-id="b08d9-103">ITSdp::put\_Url method</span></span>

<span data-ttu-id="b08d9-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b08d9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b08d9-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b08d9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b08d9-106">O método **Put \_ URL** define a URL.</span><span class="sxs-lookup"><span data-stu-id="b08d9-106">The **put\_Url** method sets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b08d9-107">Syntax</span></span>


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a><span data-ttu-id="b08d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b08d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08d9-109">*pUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b08d9-109">*pUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08d9-110">Ponteiro para uma representação **BSTR** da URL.</span><span class="sxs-lookup"><span data-stu-id="b08d9-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b08d9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b08d9-111">Return value</span></span>

<span data-ttu-id="b08d9-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b08d9-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b08d9-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b08d9-113">Return code</span></span>                                                                                   | <span data-ttu-id="b08d9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b08d9-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b08d9-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b08d9-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b08d9-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b08d9-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b08d9-118">O parâmetro *pUrl* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="b08d9-118">The *pUrl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="b08d9-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b08d9-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b08d9-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b08d9-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b08d9-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b08d9-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b08d9-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b08d9-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="b08d9-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b08d9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b08d9-125">Remarks</span></span>

<span data-ttu-id="b08d9-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PUrl* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="b08d9-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pUrl* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="b08d9-127">Uma URL é normalmente usada para fazer referência a uma página da Web que contém recursos adicionais ou informações básicas sobre uma conferência.</span><span class="sxs-lookup"><span data-stu-id="b08d9-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

<span data-ttu-id="b08d9-128">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="b08d9-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="b08d9-129">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="b08d9-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b08d9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b08d9-130">Requirements</span></span>



| <span data-ttu-id="b08d9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b08d9-131">Requirement</span></span> | <span data-ttu-id="b08d9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b08d9-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b08d9-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b08d9-133">TAPI version</span></span><br/> | <span data-ttu-id="b08d9-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b08d9-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b08d9-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b08d9-135">Header</span></span><br/>       | <dl> <span data-ttu-id="b08d9-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b08d9-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b08d9-137">Library</span></span><br/>      | <dl> <span data-ttu-id="b08d9-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b08d9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b08d9-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="b08d9-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b08d9-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b08d9-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="b08d9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08d9-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="b08d9-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="b08d9-143">**ITSdp:: obter \_ URL**</span><span class="sxs-lookup"><span data-stu-id="b08d9-143">**ITSdp::get\_Url**</span></span>](itsdp-get-url.md)
</dt> </dl>

 

