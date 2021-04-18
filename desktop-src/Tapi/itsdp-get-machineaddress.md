---
description: O \_ método Get MachineAddress Obtém o endereço do computador do host de origem.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Método ITSdp:: get_MachineAddress (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784090"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="cc5a5-103">Método ITSdp:: get \_ MachineAddress</span><span class="sxs-lookup"><span data-stu-id="cc5a5-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="cc5a5-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cc5a5-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cc5a5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cc5a5-106">O método **Get \_ MachineAddress** Obtém o endereço do computador do host de origem.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc5a5-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="cc5a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc5a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc5a5-109">*ppMachineAddress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc5a5-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5a5-110">Ponteiro para um **BSTR** que contém o endereço do computador do host de conferência.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc5a5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc5a5-111">Return value</span></span>

<span data-ttu-id="cc5a5-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cc5a5-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc5a5-113">Return code</span></span>                                                                                   | <span data-ttu-id="cc5a5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc5a5-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc5a5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cc5a5-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="cc5a5-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cc5a5-118">O parâmetro *ppMachineAddres* s não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="cc5a5-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cc5a5-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="cc5a5-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cc5a5-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cc5a5-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cc5a5-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="cc5a5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc5a5-125">Remarks</span></span>

<span data-ttu-id="cc5a5-126">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppMachineAddress* .</span><span class="sxs-lookup"><span data-stu-id="cc5a5-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="cc5a5-127">O parâmetro *ppMachineAddress* pode ser retornado como um nome DNS ("johnsmith.workinghard.Microsoft.com") ou um endereço IP ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="cc5a5-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="cc5a5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc5a5-128">Requirements</span></span>



| <span data-ttu-id="cc5a5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc5a5-129">Requirement</span></span> | <span data-ttu-id="cc5a5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="cc5a5-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5a5-131">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cc5a5-131">TAPI version</span></span><br/> | <span data-ttu-id="cc5a5-132">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cc5a5-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cc5a5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc5a5-133">Header</span></span><br/>       | <dl> <span data-ttu-id="cc5a5-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc5a5-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc5a5-135">Library</span></span><br/>      | <dl> <span data-ttu-id="cc5a5-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cc5a5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cc5a5-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="cc5a5-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a5-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc5a5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc5a5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc5a5-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="cc5a5-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="cc5a5-141">**ITSdp::p UT \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="cc5a5-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

