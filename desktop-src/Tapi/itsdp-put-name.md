---
description: O \_ método Put name define o nome da sessão.
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: 'ITSdp: método de ut_Name de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7383183b6b367d71d18070eedd5857740665fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760339"
---
# <a name="itsdpput_name-method"></a><span data-ttu-id="1850b-103">ITSdp::p \_ método de nome UT</span><span class="sxs-lookup"><span data-stu-id="1850b-103">ITSdp::put\_Name method</span></span>

<span data-ttu-id="1850b-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1850b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1850b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1850b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1850b-106">O método **Put \_ Name** define o nome da sessão.</span><span class="sxs-lookup"><span data-stu-id="1850b-106">The **put\_Name** method sets the session name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1850b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1850b-107">Syntax</span></span>


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="1850b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1850b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1850b-109">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1850b-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1850b-110">Ponteiro para um **BSTR** que contém o nome da sessão.</span><span class="sxs-lookup"><span data-stu-id="1850b-110">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1850b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1850b-111">Return value</span></span>

<span data-ttu-id="1850b-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1850b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1850b-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1850b-113">Return code</span></span>                                                                                   | <span data-ttu-id="1850b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1850b-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1850b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1850b-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1850b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1850b-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1850b-118">O parâmetro *pname* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="1850b-118">The *pName* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="1850b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1850b-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1850b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1850b-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1850b-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1850b-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1850b-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1850b-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1850b-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1850b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1850b-125">Remarks</span></span>

<span data-ttu-id="1850b-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *pname* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="1850b-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1850b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1850b-127">Requirements</span></span>



| <span data-ttu-id="1850b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1850b-128">Requirement</span></span> | <span data-ttu-id="1850b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1850b-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1850b-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1850b-130">TAPI version</span></span><br/> | <span data-ttu-id="1850b-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1850b-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1850b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1850b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="1850b-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1850b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1850b-134">Library</span></span><br/>      | <dl> <span data-ttu-id="1850b-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1850b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1850b-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="1850b-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1850b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1850b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1850b-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="1850b-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="1850b-140">**ITSdp:: obter \_ nome**</span><span class="sxs-lookup"><span data-stu-id="1850b-140">**ITSdp::get\_Name**</span></span>](itsdp-get-name.md)
</dt> </dl>

 

