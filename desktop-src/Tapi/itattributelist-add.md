---
description: O método add adiciona o atributo ao índice especificado.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'Método ITAttributeList:: Add (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781048"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="1deaa-103">Método ITAttributeList:: Add</span><span class="sxs-lookup"><span data-stu-id="1deaa-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="1deaa-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1deaa-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1deaa-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1deaa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1deaa-106">O método **Add** adiciona o atributo ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1deaa-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1deaa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1deaa-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="1deaa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1deaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1deaa-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1deaa-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1deaa-110">Índice do atributo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="1deaa-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="1deaa-111">*pAttribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1deaa-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1deaa-112">Ponteiro para um **BSTR** que contém o valor do atributo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="1deaa-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1deaa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1deaa-113">Return value</span></span>

<span data-ttu-id="1deaa-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1deaa-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1deaa-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1deaa-115">Return code</span></span>                                                                                   | <span data-ttu-id="1deaa-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1deaa-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1deaa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1deaa-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1deaa-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1deaa-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1deaa-120">O parâmetro *index* ou *pAttribute* não é válido.</span><span class="sxs-lookup"><span data-stu-id="1deaa-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="1deaa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1deaa-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1deaa-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1deaa-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1deaa-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1deaa-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1deaa-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1deaa-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1deaa-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1deaa-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1deaa-127">Remarks</span></span>

<span data-ttu-id="1deaa-128">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PAttribute* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="1deaa-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1deaa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1deaa-129">Requirements</span></span>



| <span data-ttu-id="1deaa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1deaa-130">Requirement</span></span> | <span data-ttu-id="1deaa-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1deaa-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1deaa-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1deaa-132">TAPI version</span></span><br/> | <span data-ttu-id="1deaa-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1deaa-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1deaa-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1deaa-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1deaa-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1deaa-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1deaa-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1deaa-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1deaa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1deaa-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1deaa-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1deaa-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1deaa-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1deaa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1deaa-141">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="1deaa-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

