---
description: O \_ método Put originador define o originador da conferência.
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: 'ITSdp: método de ut_Originator de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506554668e697e9281dc5dc15784fa36f7429d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757210"
---
# <a name="itsdpput_originator-method"></a><span data-ttu-id="0d717-103">Método ITSdp::p UT \_ originador</span><span class="sxs-lookup"><span data-stu-id="0d717-103">ITSdp::put\_Originator method</span></span>

<span data-ttu-id="0d717-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0d717-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0d717-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="0d717-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0d717-106">O método **Put \_ originador** define o originador da conferência.</span><span class="sxs-lookup"><span data-stu-id="0d717-106">The **put\_Originator** method sets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d717-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d717-107">Syntax</span></span>


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="0d717-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d717-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d717-109">*pOriginator* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d717-109">*pOriginator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d717-110">Ponteiro para uma representação **BSTR** do originador da conferência.</span><span class="sxs-lookup"><span data-stu-id="0d717-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d717-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d717-111">Return value</span></span>

<span data-ttu-id="0d717-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0d717-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0d717-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0d717-113">Return code</span></span>                                                                                   | <span data-ttu-id="0d717-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d717-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0d717-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0d717-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0d717-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d717-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0d717-118">O parâmetro *pOriginator* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="0d717-118">The *pOriginator* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="0d717-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0d717-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0d717-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0d717-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0d717-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="0d717-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0d717-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0d717-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="0d717-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0d717-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d717-125">Remarks</span></span>

<span data-ttu-id="0d717-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *POriginator* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="0d717-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pOriginator* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="0d717-127">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="0d717-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="0d717-128">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="0d717-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d717-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d717-129">Requirements</span></span>



| <span data-ttu-id="0d717-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d717-130">Requirement</span></span> | <span data-ttu-id="0d717-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0d717-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d717-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="0d717-132">TAPI version</span></span><br/> | <span data-ttu-id="0d717-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0d717-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0d717-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d717-134">Header</span></span><br/>       | <dl> <span data-ttu-id="0d717-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d717-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d717-136">Library</span></span><br/>      | <dl> <span data-ttu-id="0d717-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0d717-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0d717-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="0d717-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d717-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d717-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d717-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d717-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="0d717-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="0d717-142">**ITSdp:: obter \_ originador**</span><span class="sxs-lookup"><span data-stu-id="0d717-142">**ITSdp::get\_Originator**</span></span>](itsdp-get-originator.md)
</dt> </dl>

 

