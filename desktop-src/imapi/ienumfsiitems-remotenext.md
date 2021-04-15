---
title: Método IEnumFsiItems RemoteNext
description: Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração. | Método IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Método RemoteNext IMAPi
- Método RemoteNext IMAPi, interface IEnumFsiItems
- IEnumFsiItems interface IMAPi, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506414"
---
# <a name="ienumfsiitemsremotenext-method"></a><span data-ttu-id="623ca-107">Método IEnumFsiItems:: RemoteNext</span><span class="sxs-lookup"><span data-stu-id="623ca-107">IEnumFsiItems::RemoteNext method</span></span>

<span data-ttu-id="623ca-108">Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="623ca-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="623ca-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="623ca-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="623ca-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="623ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623ca-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="623ca-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623ca-112">Número de itens a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="623ca-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="623ca-113">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="623ca-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="623ca-114">Matriz de interfaces [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) .</span><span class="sxs-lookup"><span data-stu-id="623ca-114">Array of [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) interfaces.</span></span> <span data-ttu-id="623ca-115">Você deve liberar cada interface em rgelt quando terminar.</span><span class="sxs-lookup"><span data-stu-id="623ca-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="623ca-116">*pceltFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="623ca-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="623ca-117">Número de elementos retornados em rgelt.</span><span class="sxs-lookup"><span data-stu-id="623ca-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="623ca-118">Você pode definir *pceltFetched* como **NULL** se *celt* for um.</span><span class="sxs-lookup"><span data-stu-id="623ca-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="623ca-119">Caso contrário, inicialize o valor de *pceltFetched* como 0 antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="623ca-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623ca-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="623ca-120">Return value</span></span>

<span data-ttu-id="623ca-121">S \_ OK é retornado quando o número de elementos solicitados (*celt*) é retornado com êxito ou o número de itens retornados (*pceltFetched*) é menor que o número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="623ca-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="623ca-122">Outros códigos de êxito podem ser retornados como resultado da implementação.</span><span class="sxs-lookup"><span data-stu-id="623ca-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="623ca-123">Os códigos de erro a seguir são normalmente retornados na falha da operação, mas não representam os únicos valores de erro possíveis:</span><span class="sxs-lookup"><span data-stu-id="623ca-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="623ca-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="623ca-124">Return code</span></span>                                                                                   | <span data-ttu-id="623ca-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="623ca-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="623ca-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="623ca-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="623ca-127">O ponteiro não é válido.</span><span class="sxs-lookup"><span data-stu-id="623ca-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="623ca-128">Valor: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="623ca-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="623ca-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="623ca-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="623ca-130">Falha ao alocar a memória necessária.</span><span class="sxs-lookup"><span data-stu-id="623ca-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="623ca-131">Valor: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="623ca-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="623ca-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="623ca-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="623ca-133">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="623ca-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="623ca-134">Valor: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="623ca-134">Value: 0x80070057</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="623ca-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623ca-135">Requirements</span></span>



| <span data-ttu-id="623ca-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="623ca-136">Requirement</span></span> | <span data-ttu-id="623ca-137">Valor</span><span class="sxs-lookup"><span data-stu-id="623ca-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="623ca-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="623ca-138">Minimum supported client</span></span><br/> | <span data-ttu-id="623ca-139">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP2\]</span><span class="sxs-lookup"><span data-stu-id="623ca-139">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="623ca-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="623ca-140">Minimum supported server</span></span><br/> | <span data-ttu-id="623ca-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="623ca-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="623ca-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="623ca-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="623ca-143"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="623ca-143"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623ca-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="623ca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623ca-145">**IEnumFsiItems**</span><span class="sxs-lookup"><span data-stu-id="623ca-145">**IEnumFsiItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[<span data-ttu-id="623ca-146">IEnumFsiItems:: Next</span><span class="sxs-lookup"><span data-stu-id="623ca-146">IEnumFsiItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





