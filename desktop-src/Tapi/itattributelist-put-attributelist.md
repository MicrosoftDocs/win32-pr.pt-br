---
description: O \_ método Put atributolist define a lista de atributos.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: 'ITAttributeList: método de ut_AttributeList de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792628"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="771d0-103">ITAttributeList::p método de atributo de UT \_</span><span class="sxs-lookup"><span data-stu-id="771d0-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="771d0-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="771d0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="771d0-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="771d0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="771d0-106">O método **Put \_ atributolist** define a lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="771d0-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="771d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="771d0-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="771d0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="771d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771d0-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="771d0-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771d0-110">Matriz de atributos a ser definida.</span><span class="sxs-lookup"><span data-stu-id="771d0-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771d0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="771d0-111">Return value</span></span>

<span data-ttu-id="771d0-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="771d0-112">This method can return one of these values.</span></span>



| <span data-ttu-id="771d0-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="771d0-113">Return code</span></span>                                                                                   | <span data-ttu-id="771d0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="771d0-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="771d0-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="771d0-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="771d0-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="771d0-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="771d0-118">O parâmetro *newVal* não é válido.</span><span class="sxs-lookup"><span data-stu-id="771d0-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="771d0-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="771d0-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="771d0-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="771d0-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="771d0-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="771d0-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="771d0-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="771d0-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="771d0-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="771d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="771d0-125">Requirements</span></span>



| <span data-ttu-id="771d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="771d0-126">Requirement</span></span> | <span data-ttu-id="771d0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="771d0-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="771d0-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="771d0-128">TAPI version</span></span><br/> | <span data-ttu-id="771d0-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="771d0-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="771d0-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="771d0-130">Header</span></span><br/>       | <dl> <span data-ttu-id="771d0-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="771d0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="771d0-132">Library</span></span><br/>      | <dl> <span data-ttu-id="771d0-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="771d0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="771d0-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="771d0-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771d0-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="771d0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="771d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771d0-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="771d0-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="771d0-138">**ITAttributeList:: obter \_ atributolist**</span><span class="sxs-lookup"><span data-stu-id="771d0-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




