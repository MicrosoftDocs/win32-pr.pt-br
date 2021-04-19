---
description: O \_ método obter contagem Obtém o número de atributos.
ms.assetid: dc607f09-4cca-4ef0-8b86-dbc5e6edcfdd
title: 'Método ITAttributeList:: get_Count (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634996e8d920005f5da4c40b6cfca3f5cb632363
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754194"
---
# <a name="itattributelistget_count-method"></a><span data-ttu-id="6e32e-103">Método de contagem ITAttributeList:: get \_</span><span class="sxs-lookup"><span data-stu-id="6e32e-103">ITAttributeList::get\_Count method</span></span>

<span data-ttu-id="6e32e-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6e32e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6e32e-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6e32e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6e32e-106">O método **obter \_ contagem** Obtém o número de atributos.</span><span class="sxs-lookup"><span data-stu-id="6e32e-106">The **get\_Count** method gets the number of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e32e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e32e-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6e32e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e32e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e32e-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e32e-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e32e-110">Contagem dos atributos na lista.</span><span class="sxs-lookup"><span data-stu-id="6e32e-110">Count of the attributes in the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e32e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e32e-111">Return value</span></span>

<span data-ttu-id="6e32e-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6e32e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6e32e-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6e32e-113">Return code</span></span>                                                                                   | <span data-ttu-id="6e32e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e32e-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6e32e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6e32e-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6e32e-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6e32e-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6e32e-118">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="6e32e-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="6e32e-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6e32e-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="6e32e-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6e32e-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6e32e-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6e32e-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6e32e-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6e32e-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="6e32e-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="6e32e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e32e-125">Requirements</span></span>



| <span data-ttu-id="6e32e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e32e-126">Requirement</span></span> | <span data-ttu-id="6e32e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6e32e-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e32e-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6e32e-128">TAPI version</span></span><br/> | <span data-ttu-id="6e32e-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6e32e-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6e32e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e32e-130">Header</span></span><br/>       | <dl> <span data-ttu-id="6e32e-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e32e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e32e-132">Library</span></span><br/>      | <dl> <span data-ttu-id="6e32e-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6e32e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6e32e-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="6e32e-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e32e-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e32e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e32e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e32e-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="6e32e-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




