---
description: O \_ método de descrição Put define a descrição da sessão.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: 'ITSdp: método de ut_Description de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757964"
---
# <a name="itsdpput_description-method"></a><span data-ttu-id="42425-103">Método de descrição ITSdp::p UT \_</span><span class="sxs-lookup"><span data-stu-id="42425-103">ITSdp::put\_Description method</span></span>

<span data-ttu-id="42425-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="42425-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="42425-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="42425-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="42425-106">O método de **\_ Descrição Put** define a descrição da sessão.</span><span class="sxs-lookup"><span data-stu-id="42425-106">The **put\_Description** method sets the session description.</span></span>

## <a name="syntax"></a><span data-ttu-id="42425-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42425-107">Syntax</span></span>


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a><span data-ttu-id="42425-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42425-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42425-109">*pDescription* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42425-109">*pDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42425-110">Ponteiro para um **BSTR** que contém a descrição da sessão.</span><span class="sxs-lookup"><span data-stu-id="42425-110">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42425-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42425-111">Return value</span></span>

<span data-ttu-id="42425-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="42425-112">This method can return one of these values.</span></span>



| <span data-ttu-id="42425-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="42425-113">Return code</span></span>                                                                                   | <span data-ttu-id="42425-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="42425-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="42425-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42425-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="42425-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="42425-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="42425-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="42425-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="42425-118">O parâmetro *pDescription* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="42425-118">The *pDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="42425-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="42425-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="42425-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="42425-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="42425-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="42425-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="42425-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="42425-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="42425-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="42425-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="42425-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="42425-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="42425-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="42425-125">Remarks</span></span>

<span data-ttu-id="42425-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PDescription* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="42425-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pDescription* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="42425-127">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="42425-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="42425-128">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="42425-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="42425-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42425-129">Requirements</span></span>



| <span data-ttu-id="42425-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="42425-130">Requirement</span></span> | <span data-ttu-id="42425-131">Valor</span><span class="sxs-lookup"><span data-stu-id="42425-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42425-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="42425-132">TAPI version</span></span><br/> | <span data-ttu-id="42425-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="42425-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="42425-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42425-134">Header</span></span><br/>       | <dl> <span data-ttu-id="42425-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="42425-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="42425-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42425-136">Library</span></span><br/>      | <dl> <span data-ttu-id="42425-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42425-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="42425-138">DLL</span><span class="sxs-lookup"><span data-stu-id="42425-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="42425-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42425-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42425-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="42425-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42425-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="42425-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="42425-142">**ITSdp:: obter \_ Descrição**</span><span class="sxs-lookup"><span data-stu-id="42425-142">**ITSdp::get\_Description**</span></span>](itsdp-get-description.md)
</dt> </dl>

 

