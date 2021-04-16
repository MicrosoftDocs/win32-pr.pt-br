---
description: O \_ método Put SessionVersion define a versão da sessão.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: 'ITSdp: método de ut_SessionVersion de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779306"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="e9c6b-103">ITSdp: método UT \_ SessionVersion:p</span><span class="sxs-lookup"><span data-stu-id="e9c6b-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="e9c6b-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9c6b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e9c6b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e9c6b-106">O método **Put \_ SessionVersion** define a versão da sessão.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c6b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9c6b-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="e9c6b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9c6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c6b-109">*SessionVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9c6b-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c6b-110">Valor da versão da sessão.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c6b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9c6b-111">Return value</span></span>

<span data-ttu-id="e9c6b-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e9c6b-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e9c6b-113">Return code</span></span>                                                                                   | <span data-ttu-id="e9c6b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9c6b-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e9c6b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e9c6b-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e9c6b-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e9c6b-118">O parâmetro *SessionVersion* não é válido.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="e9c6b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e9c6b-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e9c6b-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e9c6b-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e9c6b-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e9c6b-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e9c6b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9c6b-125">Remarks</span></span>

<span data-ttu-id="e9c6b-126">O valor de retorno desse método pode ser **ULONG**, mas Visual Basic não dá suporte ao tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="e9c6b-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="e9c6b-127">Um **Double** é o próximo menor tipo que abrange todo o intervalo de valores necessário.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="e9c6b-128">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="e9c6b-129">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="e9c6b-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c6b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9c6b-130">Requirements</span></span>



| <span data-ttu-id="e9c6b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9c6b-131">Requirement</span></span> | <span data-ttu-id="e9c6b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e9c6b-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c6b-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e9c6b-133">TAPI version</span></span><br/> | <span data-ttu-id="e9c6b-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e9c6b-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e9c6b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9c6b-135">Header</span></span><br/>       | <dl> <span data-ttu-id="e9c6b-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9c6b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9c6b-137">Library</span></span><br/>      | <dl> <span data-ttu-id="e9c6b-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e9c6b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c6b-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="e9c6b-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c6b-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c6b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9c6b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c6b-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="e9c6b-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="e9c6b-143">**ITSdp:: obter \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="e9c6b-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




