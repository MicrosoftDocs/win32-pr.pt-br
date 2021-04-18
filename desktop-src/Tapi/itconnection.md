---
description: A funcionalidade de interface ITConnection é mostrada abaixo.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interface ITConnection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810137"
---
# <a name="itconnection-interface"></a><span data-ttu-id="6bc09-103">Interface ITConnection</span><span class="sxs-lookup"><span data-stu-id="6bc09-103">ITConnection interface</span></span>

<span data-ttu-id="6bc09-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6bc09-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6bc09-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6bc09-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6bc09-106">A interface **ITConnection** fornece a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="6bc09-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="6bc09-107">Fornece acesso ao endereço e às informações de TTL (vida útil) da sessão.</span><span class="sxs-lookup"><span data-stu-id="6bc09-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="6bc09-108">Fornece acesso às informações de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6bc09-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="6bc09-109">Habilita a manipulação da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6bc09-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="6bc09-110">A interface **ITConnection** é criada chamando **QueryInterface** no [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="6bc09-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="6bc09-111">Membros</span><span class="sxs-lookup"><span data-stu-id="6bc09-111">Members</span></span>

<span data-ttu-id="6bc09-112">A interface **ITConnection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6bc09-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6bc09-113">**ITConnection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6bc09-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="6bc09-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6bc09-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6bc09-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="6bc09-115">Methods</span></span>

<span data-ttu-id="6bc09-116">A interface **ITConnection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6bc09-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="6bc09-117">Método</span><span class="sxs-lookup"><span data-stu-id="6bc09-117">Method</span></span>                                                               | <span data-ttu-id="6bc09-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bc09-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bc09-119">**obter \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="6bc09-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="6bc09-120">Obtém o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="6bc09-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6bc09-121">**obter \_ largura de banda**</span><span class="sxs-lookup"><span data-stu-id="6bc09-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="6bc09-122">Obtém o valor da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6bc09-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="6bc09-123">**obter \_ BandwidthModifier**</span><span class="sxs-lookup"><span data-stu-id="6bc09-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="6bc09-124">Obtém o modificador de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6bc09-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="6bc09-125">**obter o \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="6bc09-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="6bc09-126">Obtém o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="6bc09-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6bc09-127">**obter \_ NumAddresses**</span><span class="sxs-lookup"><span data-stu-id="6bc09-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="6bc09-128">Obtém o número de endereços a serem usados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="6bc09-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="6bc09-129">**obter \_ StartAddress**</span><span class="sxs-lookup"><span data-stu-id="6bc09-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="6bc09-130">Obtém o primeiro endereço a ser usado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="6bc09-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="6bc09-131">**obter \_ TTL**</span><span class="sxs-lookup"><span data-stu-id="6bc09-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="6bc09-132">Obtém o escopo [*TTL (vida útil)*](t-tapgloss.md) para transmissões nos endereços.</span><span class="sxs-lookup"><span data-stu-id="6bc09-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="6bc09-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="6bc09-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="6bc09-134">Obtém a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6bc09-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="6bc09-135">**colocar \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="6bc09-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="6bc09-136">Define o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="6bc09-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6bc09-137">**colocar \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="6bc09-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="6bc09-138">Define o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="6bc09-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6bc09-139">**SetAddressInfo**</span><span class="sxs-lookup"><span data-stu-id="6bc09-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="6bc09-140">Define informações de endereço.</span><span class="sxs-lookup"><span data-stu-id="6bc09-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="6bc09-141">**SetBandwidthInfo**</span><span class="sxs-lookup"><span data-stu-id="6bc09-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="6bc09-142">Define o valor de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6bc09-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="6bc09-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="6bc09-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="6bc09-144">Define a chave de criptografia necessária para descriptografar a sessão ou uma indicação para um mecanismo para obter uma chave utilizável por meios externos.</span><span class="sxs-lookup"><span data-stu-id="6bc09-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="6bc09-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc09-145">Requirements</span></span>



| <span data-ttu-id="6bc09-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc09-146">Requirement</span></span> | <span data-ttu-id="6bc09-147">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc09-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc09-148">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6bc09-148">TAPI version</span></span><br/> | <span data-ttu-id="6bc09-149">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6bc09-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6bc09-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bc09-150">Header</span></span><br/>       | <dl> <span data-ttu-id="6bc09-151"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bc09-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6bc09-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bc09-152">Library</span></span><br/>      | <dl> <span data-ttu-id="6bc09-153"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bc09-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6bc09-154">DLL</span><span class="sxs-lookup"><span data-stu-id="6bc09-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="6bc09-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bc09-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

