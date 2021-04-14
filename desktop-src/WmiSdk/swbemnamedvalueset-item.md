---
description: O método item do objeto SWbemNamedValueSet Obtém um objeto SWbemNamedValue da coleção.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505669"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="d3033-103">Método SWbemNamedValueSet. Item</span><span class="sxs-lookup"><span data-stu-id="d3033-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="d3033-104">O método **Item** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) Obtém um objeto [**SWbemNamedValue**](swbemnamedvalue.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="d3033-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="d3033-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d3033-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3033-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3033-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d3033-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3033-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3033-108">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3033-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3033-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d3033-109">Required.</span></span> <span data-ttu-id="d3033-110">Nome do valor a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d3033-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d3033-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d3033-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3033-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d3033-112">Reserved.</span></span> <span data-ttu-id="d3033-113">Esse valor deve ser zero, se especificado.</span><span class="sxs-lookup"><span data-stu-id="d3033-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3033-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3033-114">Return value</span></span>

<span data-ttu-id="d3033-115">Se for bem-sucedido, o objeto [**SWbemNamedValue**](swbemnamedvalue.md) solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="d3033-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3033-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d3033-116">Error codes</span></span>

<span data-ttu-id="d3033-117">Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3033-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d3033-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d3033-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d3033-119">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="d3033-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d3033-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d3033-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d3033-121">Um parâmetro inválido foi especificado ou o namespace não pôde ser analisado.</span><span class="sxs-lookup"><span data-stu-id="d3033-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="d3033-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d3033-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d3033-123">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="d3033-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d3033-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d3033-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d3033-125">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d3033-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3033-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3033-126">Remarks</span></span>

<span data-ttu-id="d3033-127">Para obter exemplos de como adicionar e recuperar valores nomeados, consulte [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="d3033-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3033-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3033-128">Requirements</span></span>



| <span data-ttu-id="d3033-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3033-129">Requirement</span></span> | <span data-ttu-id="d3033-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d3033-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3033-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3033-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d3033-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3033-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3033-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3033-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d3033-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3033-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3033-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3033-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3033-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3033-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3033-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d3033-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3033-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d3033-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d3033-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d3033-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3033-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3033-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3033-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="d3033-141">CLSID</span></span><br/>                    | <span data-ttu-id="d3033-142">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="d3033-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="d3033-143">IID</span><span class="sxs-lookup"><span data-stu-id="d3033-143">IID</span></span><br/>                      | <span data-ttu-id="d3033-144">ISWbemNamedValueSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="d3033-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="d3033-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3033-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3033-146">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="d3033-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




