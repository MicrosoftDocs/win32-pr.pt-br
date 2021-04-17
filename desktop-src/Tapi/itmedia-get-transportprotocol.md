---
description: O \_ método Get TransportProtocol Obtém o protocolo de transporte.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'Método ITMedia:: get_TransportProtocol (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789864"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="5f016-103">Método ITMedia:: get \_ TransportProtocol</span><span class="sxs-lookup"><span data-stu-id="5f016-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="5f016-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5f016-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5f016-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="5f016-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5f016-106">O método **Get \_ TransportProtocol** Obtém o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="5f016-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="5f016-107">Isso é especificado além do formato de mídia para que o mesmo formato de mídia padrão possa ser transportado por protocolos de transporte diferentes, mesmo quando o protocolo de rede for o mesmo, como com áudio PCM de IVA e áudio RTP PCM.</span><span class="sxs-lookup"><span data-stu-id="5f016-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f016-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f016-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="5f016-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f016-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f016-110">*ppProtocol* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f016-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f016-111">Ponteiro para a representação **BSTR** do protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="5f016-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f016-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f016-112">Return value</span></span>

<span data-ttu-id="5f016-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="5f016-113">This method can return one of these values.</span></span>



| <span data-ttu-id="5f016-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5f016-114">Return code</span></span>                                                                                   | <span data-ttu-id="5f016-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f016-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5f016-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5f016-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5f016-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5f016-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5f016-119">O parâmetro *ppProtocol* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="5f016-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="5f016-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5f016-121">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="5f016-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5f016-122"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5f016-123">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="5f016-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5f016-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5f016-125">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="5f016-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5f016-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f016-126">Remarks</span></span>

<span data-ttu-id="5f016-127">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppProtocol* .</span><span class="sxs-lookup"><span data-stu-id="5f016-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f016-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f016-128">Requirements</span></span>



| <span data-ttu-id="5f016-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f016-129">Requirement</span></span> | <span data-ttu-id="5f016-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5f016-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f016-131">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5f016-131">TAPI version</span></span><br/> | <span data-ttu-id="5f016-132">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5f016-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5f016-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f016-133">Header</span></span><br/>       | <dl> <span data-ttu-id="5f016-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f016-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f016-135">Library</span></span><br/>      | <dl> <span data-ttu-id="5f016-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5f016-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5f016-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="5f016-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f016-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f016-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f016-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f016-140">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="5f016-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="5f016-141">**ITMedia::p UT \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="5f016-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

