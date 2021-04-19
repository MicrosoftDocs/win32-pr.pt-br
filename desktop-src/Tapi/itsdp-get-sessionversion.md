---
description: O \_ método Get SessionVersion Obtém o valor de 32 bits (ideal protocolo NTP ou NTP) que serve como a versão da sessão.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Método ITSdp:: get_SessionVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753540"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="ae2ac-103">Método ITSdp:: get \_ SessionVersion</span><span class="sxs-lookup"><span data-stu-id="ae2ac-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="ae2ac-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ae2ac-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ae2ac-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ae2ac-106">O método **Get \_ SessionVersion** Obtém o valor de 32 bits (ideal protocolo NTP ou NTP) que serve como a versão da sessão.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="ae2ac-107">Embora isso seja gerado automaticamente quando a sessão é criada, o usuário é responsável por alterá-lo quando o SDP é modificado.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2ac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae2ac-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="ae2ac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae2ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2ac-110">*pSessionVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ae2ac-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2ac-111">Ponteiro para o identificador de versão da sessão.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2ac-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae2ac-112">Return value</span></span>

<span data-ttu-id="ae2ac-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-113">This method can return one of these values.</span></span>



| <span data-ttu-id="ae2ac-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ae2ac-114">Return code</span></span>                                                                                   | <span data-ttu-id="ae2ac-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae2ac-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae2ac-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ae2ac-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="ae2ac-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ae2ac-119">O parâmetro *pSessionVersion* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="ae2ac-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ae2ac-121">O parâmetro *pSessionVersion* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="ae2ac-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ae2ac-123">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="ae2ac-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ae2ac-125">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ae2ac-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ae2ac-127">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ae2ac-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae2ac-128">Remarks</span></span>

<span data-ttu-id="ae2ac-129">O valor de retorno desse método pode ser **ULONG**, mas Visual Basic não dá suporte ao tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="ae2ac-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="ae2ac-130">Um **Double** é o próximo menor tipo que abrange todo o intervalo de valores necessário.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2ac-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae2ac-131">Requirements</span></span>



| <span data-ttu-id="ae2ac-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2ac-132">Requirement</span></span> | <span data-ttu-id="ae2ac-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ae2ac-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2ac-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ae2ac-134">TAPI version</span></span><br/> | <span data-ttu-id="ae2ac-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ae2ac-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ae2ac-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae2ac-136">Header</span></span><br/>       | <dl> <span data-ttu-id="ae2ac-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae2ac-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae2ac-138">Library</span></span><br/>      | <dl> <span data-ttu-id="ae2ac-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ae2ac-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ae2ac-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="ae2ac-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2ac-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae2ac-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2ac-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ae2ac-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="ae2ac-144">**ITSdp::p UT \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="ae2ac-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




