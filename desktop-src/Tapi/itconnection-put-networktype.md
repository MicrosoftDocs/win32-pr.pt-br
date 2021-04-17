---
description: O \_ método Put NetworkType define o tipo de rede.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: 'ITConnection: método de ut_NetworkType de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761360"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="17497-103">Método ITConnection::p UT \_ NetworkType</span><span class="sxs-lookup"><span data-stu-id="17497-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="17497-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="17497-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="17497-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="17497-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="17497-106">O método **Put \_ NetworkType** define o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="17497-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="17497-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17497-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="17497-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17497-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17497-109">*pNetworkType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17497-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17497-110">Ponteiro para um **BSTR** que contém o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="17497-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17497-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17497-111">Return value</span></span>

<span data-ttu-id="17497-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="17497-112">This method can return one of these values.</span></span>



| <span data-ttu-id="17497-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="17497-113">Return code</span></span>                                                                                   | <span data-ttu-id="17497-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="17497-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="17497-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17497-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="17497-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="17497-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="17497-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="17497-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="17497-118">O parâmetro *pNetworkType* não é válido.</span><span class="sxs-lookup"><span data-stu-id="17497-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="17497-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="17497-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="17497-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="17497-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="17497-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="17497-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="17497-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="17497-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="17497-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="17497-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="17497-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="17497-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="17497-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="17497-125">Remarks</span></span>

<span data-ttu-id="17497-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PNetworkType* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="17497-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="17497-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17497-127">Requirements</span></span>



| <span data-ttu-id="17497-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="17497-128">Requirement</span></span> | <span data-ttu-id="17497-129">Valor</span><span class="sxs-lookup"><span data-stu-id="17497-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17497-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="17497-130">TAPI version</span></span><br/> | <span data-ttu-id="17497-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="17497-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="17497-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17497-132">Header</span></span><br/>       | <dl> <span data-ttu-id="17497-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="17497-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="17497-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17497-134">Library</span></span><br/>      | <dl> <span data-ttu-id="17497-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17497-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="17497-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17497-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="17497-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17497-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17497-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="17497-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17497-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="17497-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="17497-140">**ITConnection:: obter o \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="17497-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

