---
description: O método Create cria um novo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'Método ITTimeCollection:: Create (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811926"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="a4723-103">Método ITTimeCollection:: Create</span><span class="sxs-lookup"><span data-stu-id="a4723-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="a4723-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4723-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4723-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a4723-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a4723-106">O método **Create** cria um novo componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="a4723-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4723-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4723-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="a4723-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4723-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a4723-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4723-110">Índice do item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a4723-110">Index of the item to create.</span></span> <span data-ttu-id="a4723-111">(A matriz de índice é baseada em um.)</span><span class="sxs-lookup"><span data-stu-id="a4723-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="a4723-112">*ppTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4723-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4723-113">Ponteiro para o componente b criado.</span><span class="sxs-lookup"><span data-stu-id="a4723-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4723-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4723-114">Return value</span></span>

<span data-ttu-id="a4723-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a4723-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a4723-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a4723-116">Value</span></span>                                                                                         | <span data-ttu-id="a4723-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a4723-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a4723-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a4723-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a4723-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a4723-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a4723-121">O parâmetro *ppTime* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="a4723-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="a4723-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a4723-123">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="a4723-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="a4723-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a4723-125">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a4723-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a4723-126"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a4723-127">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a4723-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a4723-128"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a4723-129">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="a4723-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a4723-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4723-130">Remarks</span></span>

<span data-ttu-id="a4723-131">A TAPI chama o método **AddRef** na interface [**ITTime**](ittime.md) retornada por **ITTimeCollection:: Create**.</span><span class="sxs-lookup"><span data-stu-id="a4723-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="a4723-132">O aplicativo deve chamar **Release** na interface v para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="a4723-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="a4723-133">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="a4723-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="a4723-134">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="a4723-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4723-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4723-135">Requirements</span></span>



| <span data-ttu-id="a4723-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4723-136">Requirement</span></span> | <span data-ttu-id="a4723-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a4723-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4723-138">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a4723-138">TAPI version</span></span><br/> | <span data-ttu-id="a4723-139">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a4723-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a4723-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4723-140">Header</span></span><br/>       | <dl> <span data-ttu-id="a4723-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4723-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4723-142">Library</span></span><br/>      | <dl> <span data-ttu-id="a4723-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a4723-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a4723-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="a4723-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4723-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4723-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4723-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4723-147">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="a4723-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="a4723-148">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="a4723-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




