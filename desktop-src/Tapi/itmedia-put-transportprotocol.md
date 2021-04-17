---
description: O \_ método Put TransportProtocol define o protocolo de transporte.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: 'ITMedia: método de ut_TransportProtocol de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789863"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="1f520-103">ITMedia: método UT \_ TransportProtocol:p</span><span class="sxs-lookup"><span data-stu-id="1f520-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="1f520-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1f520-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1f520-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1f520-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1f520-106">O método **Put \_ TransportProtocol** define o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f520-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="1f520-107">Isso é especificado além do formato de mídia para que o mesmo formato de mídia padrão possa ser transportado por protocolos de transporte diferentes, mesmo quando o protocolo de rede for o mesmo, como com áudio PCM de IVA e áudio RTP PCM.</span><span class="sxs-lookup"><span data-stu-id="1f520-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f520-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f520-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="1f520-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f520-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f520-110">*pProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f520-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f520-111">Ponteiro para um **BSTR** que contém o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f520-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f520-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f520-112">Return value</span></span>

<span data-ttu-id="1f520-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1f520-113">This method can return one of these values.</span></span>



| <span data-ttu-id="1f520-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1f520-114">Return code</span></span>                                                                                   | <span data-ttu-id="1f520-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f520-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1f520-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1f520-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1f520-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1f520-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1f520-119">O parâmetro *pProtocol* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="1f520-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="1f520-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1f520-121">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1f520-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1f520-122"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1f520-123">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1f520-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1f520-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1f520-125">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1f520-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1f520-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f520-126">Remarks</span></span>

<span data-ttu-id="1f520-127">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PProtocol* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="1f520-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="1f520-128">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="1f520-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="1f520-129">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="1f520-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f520-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f520-130">Requirements</span></span>



| <span data-ttu-id="1f520-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f520-131">Requirement</span></span> | <span data-ttu-id="1f520-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1f520-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f520-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1f520-133">TAPI version</span></span><br/> | <span data-ttu-id="1f520-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1f520-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1f520-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f520-135">Header</span></span><br/>       | <dl> <span data-ttu-id="1f520-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f520-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f520-137">Library</span></span><br/>      | <dl> <span data-ttu-id="1f520-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1f520-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1f520-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="1f520-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f520-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f520-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f520-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f520-142">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="1f520-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="1f520-143">**ITMedia:: obter \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="1f520-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

