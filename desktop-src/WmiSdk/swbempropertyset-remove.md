---
description: O método remove do objeto SWbemPropertySet exclui uma propriedade da coleção SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091286"
---
# <a name="swbempropertysetremove-method"></a><span data-ttu-id="9a51b-103">Método SWbemPropertySet. Remove</span><span class="sxs-lookup"><span data-stu-id="9a51b-103">SWbemPropertySet.Remove method</span></span>

<span data-ttu-id="9a51b-104">O método **Remove** do objeto [**SWbemPropertySet**](swbempropertyset.md) exclui uma propriedade da coleção **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="9a51b-104">The **Remove** method of the [**SWbemPropertySet**](swbempropertyset.md) object deletes a property from the **SWbemPropertySet** collection.</span></span>

<span data-ttu-id="9a51b-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9a51b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a51b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a51b-106">Syntax</span></span>


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9a51b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a51b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a51b-108">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a51b-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="9a51b-109">Required.</span></span> <span data-ttu-id="9a51b-110">Nome do item a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9a51b-110">Name of the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9a51b-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9a51b-112">Reserved.</span></span> <span data-ttu-id="9a51b-113">Esse valor deve ser 0 (zero) se especificado.</span><span class="sxs-lookup"><span data-stu-id="9a51b-113">This value must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a51b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a51b-114">Return value</span></span>

<span data-ttu-id="9a51b-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9a51b-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a51b-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9a51b-116">Error codes</span></span>

<span data-ttu-id="9a51b-117">Após a conclusão do método **Remove** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a51b-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9a51b-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9a51b-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-119">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="9a51b-119">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-120">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="9a51b-120">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-121">O usuário tentou excluir uma propriedade que não pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="9a51b-121">User attempted to delete a property that cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9a51b-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-123">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="9a51b-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="9a51b-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-125">A propriedade especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="9a51b-125">Specified property does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-126">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9a51b-126">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-127">Não há memória suficiente para execução deste método.</span><span class="sxs-lookup"><span data-stu-id="9a51b-127">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-128">**wbemErrPropagatedProperty** -142927303552 (0x2147219380)</span><span class="sxs-lookup"><span data-stu-id="9a51b-128">**wbemErrPropagatedProperty** - 142927303552 (0x2147219380)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-129">O usuário tentou excluir uma propriedade que não era de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9a51b-129">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="9a51b-130">A propriedade foi herdada de uma classe pai.</span><span class="sxs-lookup"><span data-stu-id="9a51b-130">The property was inherited from a parent class.</span></span>

</dd> <dt>

<span data-ttu-id="9a51b-131">**wbemErrResetToDefault** -2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="9a51b-131">**wbemErrResetToDefault** - 2147758082 (0x80043002)</span></span>
</dt> <dd>

<span data-ttu-id="9a51b-132">O usuário excluiu um valor padrão de substituição para a classe atual.</span><span class="sxs-lookup"><span data-stu-id="9a51b-132">User deleted an override default value for the current class.</span></span> <span data-ttu-id="9a51b-133">O valor padrão para essa propriedade na classe pai foi reativado.</span><span class="sxs-lookup"><span data-stu-id="9a51b-133">The default value for this property in the parent class has been reactivated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a51b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a51b-134">Remarks</span></span>

<span data-ttu-id="9a51b-135">As propriedades não podem ser removidas de instâncias de classe ou classes derivadas com propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9a51b-135">Properties cannot be removed from class instances or derived classes with inherited properties.</span></span> <span data-ttu-id="9a51b-136">Essas tentativas de exclusão geram um erro e a propriedade não é removida; a propriedade é redefinida para seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="9a51b-136">Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.</span></span>

<span data-ttu-id="9a51b-137">Não é possível iterar uma coleção durante a remoção de itens porque, quando você remove um elemento de uma coleção, o ponteiro da coleção é movido para o próximo elemento.</span><span class="sxs-lookup"><span data-stu-id="9a51b-137">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="9a51b-138">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="9a51b-138">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9a51b-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a51b-139">Examples</span></span>

<span data-ttu-id="9a51b-140">Para obter um exemplo de código que usa esse método, consulte o tópico [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="9a51b-140">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a51b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a51b-141">Requirements</span></span>



| <span data-ttu-id="9a51b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a51b-142">Requirement</span></span> | <span data-ttu-id="9a51b-143">Valor</span><span class="sxs-lookup"><span data-stu-id="9a51b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a51b-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a51b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9a51b-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a51b-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a51b-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a51b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9a51b-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a51b-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a51b-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a51b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a51b-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a51b-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a51b-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9a51b-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a51b-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a51b-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a51b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9a51b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a51b-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a51b-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a51b-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="9a51b-154">CLSID</span></span><br/>                    | <span data-ttu-id="9a51b-155">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="9a51b-155">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="9a51b-156">IID</span><span class="sxs-lookup"><span data-stu-id="9a51b-156">IID</span></span><br/>                      | <span data-ttu-id="9a51b-157">ISWbemPropertySet de IID \_</span><span class="sxs-lookup"><span data-stu-id="9a51b-157">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="9a51b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a51b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a51b-159">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9a51b-159">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="9a51b-160">**SWbemPropertySet. Add**</span><span class="sxs-lookup"><span data-stu-id="9a51b-160">**SWbemPropertySet.Add**</span></span>](swbempropertyset-add.md)
</dt> </dl>

 

 




