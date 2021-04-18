---
description: O método remove do objeto SWbemNamedValueSet exclui um valor nomeado do contexto.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771519"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="f2a8f-103">Método SWbemNamedValueSet. Remove</span><span class="sxs-lookup"><span data-stu-id="f2a8f-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="f2a8f-104">O método **Remove** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) exclui um valor nomeado do contexto.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="f2a8f-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2a8f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a8f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2a8f-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f2a8f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2a8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2a8f-108">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2a8f-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a8f-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-109">Required.</span></span> <span data-ttu-id="f2a8f-110">Nome do valor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="f2a8f-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f2a8f-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a8f-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-112">Reserved.</span></span> <span data-ttu-id="f2a8f-113">Esse valor deve ser zero, se especificado.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2a8f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2a8f-114">Return value</span></span>

<span data-ttu-id="f2a8f-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2a8f-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f2a8f-116">Error codes</span></span>

<span data-ttu-id="f2a8f-117">Após a conclusão do método **Remove** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f2a8f-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f2a8f-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f2a8f-119">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f2a8f-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f2a8f-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f2a8f-121">Um parâmetro inválido foi especificado ou o namespace não pôde ser analisado.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="f2a8f-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f2a8f-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f2a8f-123">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2a8f-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2a8f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2a8f-124">Requirements</span></span>



| <span data-ttu-id="f2a8f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2a8f-125">Requirement</span></span> | <span data-ttu-id="f2a8f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f2a8f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a8f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2a8f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a8f-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2a8f-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2a8f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2a8f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a8f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2a8f-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2a8f-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2a8f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2a8f-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2a8f-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2a8f-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f2a8f-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2a8f-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2a8f-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2a8f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2a8f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2a8f-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2a8f-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2a8f-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2a8f-137">CLSID</span></span><br/>                    | <span data-ttu-id="f2a8f-138">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="f2a8f-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="f2a8f-139">IID</span><span class="sxs-lookup"><span data-stu-id="f2a8f-139">IID</span></span><br/>                      | <span data-ttu-id="f2a8f-140">ISWbemNamedValueSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="f2a8f-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="f2a8f-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2a8f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a8f-142">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="f2a8f-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




