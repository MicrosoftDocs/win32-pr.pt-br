---
description: O método remove do objeto SWbemQualifierSet exclui um qualificador nomeado da coleção.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505667"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="764e2-103">Método SWbemQualifierSet. Remove</span><span class="sxs-lookup"><span data-stu-id="764e2-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="764e2-104">O método **Remove** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) exclui um qualificador nomeado da coleção.</span><span class="sxs-lookup"><span data-stu-id="764e2-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="764e2-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="764e2-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="764e2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="764e2-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="764e2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="764e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764e2-108">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="764e2-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764e2-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="764e2-109">Required.</span></span> <span data-ttu-id="764e2-110">Nome do qualificador a ser removido.</span><span class="sxs-lookup"><span data-stu-id="764e2-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="764e2-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="764e2-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="764e2-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="764e2-112">Reserved.</span></span> <span data-ttu-id="764e2-113">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="764e2-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764e2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="764e2-114">Return value</span></span>

<span data-ttu-id="764e2-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="764e2-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="764e2-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="764e2-116">Error codes</span></span>

<span data-ttu-id="764e2-117">Após a conclusão do método **Remove** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="764e2-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="764e2-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="764e2-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="764e2-119">O parâmetro *iFlags* não era válido.</span><span class="sxs-lookup"><span data-stu-id="764e2-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="764e2-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="764e2-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="764e2-121">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="764e2-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="764e2-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="764e2-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="764e2-123">O qualificador especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="764e2-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="764e2-124">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="764e2-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="764e2-125">A remoção deste qualificador é inválida.</span><span class="sxs-lookup"><span data-stu-id="764e2-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="764e2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="764e2-126">Remarks</span></span>

<span data-ttu-id="764e2-127">Não é possível iterar uma coleção durante a remoção de itens porque, quando você remove um elemento de uma coleção, o ponteiro da coleção é movido para o próximo elemento.</span><span class="sxs-lookup"><span data-stu-id="764e2-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="764e2-128">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="764e2-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="764e2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="764e2-129">Requirements</span></span>



| <span data-ttu-id="764e2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="764e2-130">Requirement</span></span> | <span data-ttu-id="764e2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="764e2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="764e2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="764e2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="764e2-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="764e2-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="764e2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="764e2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="764e2-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="764e2-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="764e2-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="764e2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="764e2-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="764e2-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="764e2-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="764e2-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="764e2-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="764e2-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="764e2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="764e2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="764e2-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="764e2-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="764e2-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="764e2-142">CLSID</span></span><br/>                    | <span data-ttu-id="764e2-143">\_SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="764e2-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="764e2-144">IID</span><span class="sxs-lookup"><span data-stu-id="764e2-144">IID</span></span><br/>                      | <span data-ttu-id="764e2-145">ISWbemQualifierSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="764e2-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="764e2-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="764e2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764e2-147">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="764e2-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="764e2-148">**SWbemQualifierSet. Add**</span><span class="sxs-lookup"><span data-stu-id="764e2-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




