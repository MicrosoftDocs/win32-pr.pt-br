---
description: O \_ método Put MediaTitle define um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'ITMedia: método de ut_MediaTitle de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760163"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="b6b9c-105">ITMedia: método UT \_ MediaTitle:p</span><span class="sxs-lookup"><span data-stu-id="b6b9c-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="b6b9c-106">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b6b9c-107">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b6b9c-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b6b9c-108">O método **Put \_ MediaTitle** define um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="b6b9c-109">Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="b6b9c-110">Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="b6b9c-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b9c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6b9c-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="b6b9c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6b9c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b9c-113">*pMediaTitle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6b9c-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b9c-114">Ponteiro para um **BSTR** que contém o título da mídia.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b9c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6b9c-115">Return value</span></span>

<span data-ttu-id="b6b9c-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b6b9c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b6b9c-117">Return code</span></span>                                                                                   | <span data-ttu-id="b6b9c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6b9c-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b6b9c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b6b9c-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b6b9c-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b6b9c-122">O parâmetro *pMediaTitle* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="b6b9c-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b6b9c-124">O parâmetro *pMediaTitle* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="b6b9c-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b6b9c-126">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b6b9c-127"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b6b9c-128">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b6b9c-129"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b6b9c-130">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b6b9c-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6b9c-131">Remarks</span></span>

<span data-ttu-id="b6b9c-132">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PMediaTitle* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="b6b9c-133">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="b6b9c-134">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="b6b9c-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b9c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6b9c-135">Requirements</span></span>



| <span data-ttu-id="b6b9c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b9c-136">Requirement</span></span> | <span data-ttu-id="b6b9c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b6b9c-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b9c-138">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b6b9c-138">TAPI version</span></span><br/> | <span data-ttu-id="b6b9c-139">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b6b9c-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b6b9c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6b9c-140">Header</span></span><br/>       | <dl> <span data-ttu-id="b6b9c-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6b9c-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6b9c-142">Library</span></span><br/>      | <dl> <span data-ttu-id="b6b9c-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b6b9c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b9c-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="b6b9c-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9c-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b9c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6b9c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b9c-147">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="b6b9c-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="b6b9c-148">**ITMedia:: obter \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="b6b9c-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

