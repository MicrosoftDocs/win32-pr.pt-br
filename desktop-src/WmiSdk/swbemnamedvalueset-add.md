---
description: O método Add do objeto SWbemNamedValueSet adiciona um objeto SWbemNamedValue à coleção. Se um elemento já existir na coleção com o mesmo nome, o novo elemento o substituirá.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505670"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="84a31-104">Método SWbemNamedValueSet. Add</span><span class="sxs-lookup"><span data-stu-id="84a31-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="84a31-105">O método **Add** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) adiciona um objeto [**SWbemNamedValue**](swbemnamedvalue.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="84a31-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="84a31-106">Se um elemento já existir na coleção com o mesmo nome, o novo elemento o substituirá.</span><span class="sxs-lookup"><span data-stu-id="84a31-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="84a31-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="84a31-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84a31-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84a31-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="84a31-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84a31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a31-110">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84a31-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84a31-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="84a31-111">Required.</span></span> <span data-ttu-id="84a31-112">Nome do novo valor.</span><span class="sxs-lookup"><span data-stu-id="84a31-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="84a31-113">*varVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84a31-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84a31-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="84a31-114">Required.</span></span> <span data-ttu-id="84a31-115">Variant que representa o novo valor.</span><span class="sxs-lookup"><span data-stu-id="84a31-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="84a31-116">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="84a31-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84a31-117">Reservado e deve ser definido como zero se especificado.</span><span class="sxs-lookup"><span data-stu-id="84a31-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a31-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84a31-118">Return value</span></span>

<span data-ttu-id="84a31-119">Se for bem-sucedido, esse método retornará o objeto [**SWbemNamedValue**](swbemnamedvalue.md) recém modificado ou recém-criado.</span><span class="sxs-lookup"><span data-stu-id="84a31-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="84a31-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="84a31-120">Remarks</span></span>

<span data-ttu-id="84a31-121">Para obter exemplos de como adicionar e recuperar valores nomeados, consulte [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="84a31-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84a31-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84a31-122">Requirements</span></span>



| <span data-ttu-id="84a31-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a31-123">Requirement</span></span> | <span data-ttu-id="84a31-124">Valor</span><span class="sxs-lookup"><span data-stu-id="84a31-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84a31-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84a31-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84a31-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84a31-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84a31-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84a31-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84a31-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84a31-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84a31-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84a31-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a31-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a31-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="84a31-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="84a31-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="84a31-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84a31-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="84a31-133">DLL</span><span class="sxs-lookup"><span data-stu-id="84a31-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84a31-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84a31-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="84a31-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="84a31-135">CLSID</span></span><br/>                    | <span data-ttu-id="84a31-136">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="84a31-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="84a31-137">IID</span><span class="sxs-lookup"><span data-stu-id="84a31-137">IID</span></span><br/>                      | <span data-ttu-id="84a31-138">ISWbemNamedValueSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="84a31-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="84a31-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="84a31-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a31-140">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="84a31-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




