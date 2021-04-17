---
description: O \_ método Get Item retorna o atributo especificado pelo índice.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'Método ITAttributeList:: get_Item (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761823"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="9f6c1-103">Método ITAttributeList:: get \_ Item</span><span class="sxs-lookup"><span data-stu-id="9f6c1-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="9f6c1-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9f6c1-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="9f6c1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9f6c1-106">O método **Get \_ Item** retorna o atributo especificado pelo índice.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6c1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f6c1-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9f6c1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f6c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6c1-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9f6c1-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6c1-110">Índice do item a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="9f6c1-111">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9f6c1-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6c1-112">Ponteiro para um **BSTR** que contém os valores do item.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6c1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f6c1-113">Return value</span></span>

<span data-ttu-id="9f6c1-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9f6c1-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9f6c1-115">Return code</span></span>                                                                                   | <span data-ttu-id="9f6c1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f6c1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9f6c1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9f6c1-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9f6c1-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9f6c1-120">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="9f6c1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9f6c1-122">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="9f6c1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9f6c1-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9f6c1-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9f6c1-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9f6c1-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9f6c1-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="9f6c1-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9f6c1-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f6c1-129">Remarks</span></span>

<span data-ttu-id="9f6c1-130">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *PVal* .</span><span class="sxs-lookup"><span data-stu-id="9f6c1-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6c1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f6c1-131">Requirements</span></span>



| <span data-ttu-id="9f6c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f6c1-132">Requirement</span></span> | <span data-ttu-id="9f6c1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9f6c1-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6c1-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="9f6c1-134">TAPI version</span></span><br/> | <span data-ttu-id="9f6c1-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9f6c1-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9f6c1-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f6c1-136">Header</span></span><br/>       | <dl> <span data-ttu-id="9f6c1-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f6c1-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f6c1-138">Library</span></span><br/>      | <dl> <span data-ttu-id="9f6c1-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9f6c1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6c1-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="9f6c1-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f6c1-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6c1-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f6c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6c1-143">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="9f6c1-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

