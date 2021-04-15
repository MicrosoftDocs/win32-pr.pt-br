---
description: O \_ método Put MachineAddress define o endereço do computador do host de origem.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'ITSdp: método de ut_MachineAddress de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753541"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="cc229-103">ITSdp: método UT \_ MachineAddress:p</span><span class="sxs-lookup"><span data-stu-id="cc229-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="cc229-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cc229-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cc229-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cc229-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cc229-106">O método **Put \_ MachineAddress** define o endereço do computador do host de origem.</span><span class="sxs-lookup"><span data-stu-id="cc229-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc229-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc229-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="cc229-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc229-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc229-109">*pMachineAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc229-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc229-110">Ponteiro para um **BSTR** que contém o endereço do computador do host de conferência.</span><span class="sxs-lookup"><span data-stu-id="cc229-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc229-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc229-111">Return value</span></span>

<span data-ttu-id="cc229-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cc229-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cc229-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc229-113">Return code</span></span>                                                                                   | <span data-ttu-id="cc229-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc229-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc229-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cc229-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cc229-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cc229-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cc229-118">O parâmetro *pMachineAddress* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="cc229-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="cc229-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cc229-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="cc229-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="cc229-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cc229-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="cc229-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="cc229-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cc229-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="cc229-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="cc229-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc229-125">Remarks</span></span>

<span data-ttu-id="cc229-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PMachineAddress* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="cc229-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="cc229-127">O parâmetro *pMachineAddress* pode ser um nome DNS ("johnsmith.workinghard.Microsoft.com") ou um endereço IP ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="cc229-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="cc229-128">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="cc229-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="cc229-129">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="cc229-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc229-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc229-130">Requirements</span></span>



| <span data-ttu-id="cc229-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc229-131">Requirement</span></span> | <span data-ttu-id="cc229-132">Valor</span><span class="sxs-lookup"><span data-stu-id="cc229-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc229-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cc229-133">TAPI version</span></span><br/> | <span data-ttu-id="cc229-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cc229-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cc229-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc229-135">Header</span></span><br/>       | <dl> <span data-ttu-id="cc229-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc229-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc229-137">Library</span></span><br/>      | <dl> <span data-ttu-id="cc229-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cc229-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cc229-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="cc229-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc229-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc229-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc229-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc229-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="cc229-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="cc229-143">**ITSdp:: obter \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="cc229-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

