---
description: O \_ método Get ProtocolVersion Obtém o protocolo de descritor de sessão (SDP; consulte a versão do protocolo RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Método ITSdp:: get_ProtocolVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768576"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="8231f-103">Método ITSdp:: get \_ ProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="8231f-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="8231f-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8231f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8231f-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8231f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8231f-106">O método **Get \_ ProtocolVersion** Obtém o protocolo de descritor de sessão (SDP; consulte a versão do protocolo RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="8231f-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="8231f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8231f-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="8231f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8231f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8231f-109">*pProtocolVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8231f-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8231f-110">Ponteiro para a versão do protocolo.</span><span class="sxs-lookup"><span data-stu-id="8231f-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8231f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8231f-111">Return value</span></span>

<span data-ttu-id="8231f-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8231f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8231f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8231f-113">Return code</span></span>                                                                                   | <span data-ttu-id="8231f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8231f-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="8231f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8231f-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8231f-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="8231f-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8231f-118">O parâmetro *pProtocolVersion* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="8231f-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="8231f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8231f-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8231f-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="8231f-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8231f-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8231f-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="8231f-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8231f-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="8231f-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="8231f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8231f-125">Requirements</span></span>



| <span data-ttu-id="8231f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8231f-126">Requirement</span></span> | <span data-ttu-id="8231f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8231f-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8231f-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8231f-128">TAPI version</span></span><br/> | <span data-ttu-id="8231f-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8231f-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8231f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8231f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8231f-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8231f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8231f-132">Library</span></span><br/>      | <dl> <span data-ttu-id="8231f-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8231f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8231f-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="8231f-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8231f-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8231f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8231f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8231f-137">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="8231f-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




