---
description: O método Add do objeto SWbemPropertySet adiciona um objeto SWbemProperty à coleção SWbemPropertySet. Se já existir uma propriedade com o mesmo nome na coleção, seu conteúdo será substituído pela nova definição.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814421"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="a4132-104">Método SWbemPropertySet. Add</span><span class="sxs-lookup"><span data-stu-id="a4132-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="a4132-105">O método **Add** do objeto [**SWbemPropertySet**](swbempropertyset.md) adiciona um objeto [**SWbemProperty**](swbemproperty.md) à coleção **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="a4132-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="a4132-106">Se já existir uma propriedade com o mesmo nome na coleção, seu conteúdo será substituído pela nova definição.</span><span class="sxs-lookup"><span data-stu-id="a4132-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="a4132-107">O valor da propriedade adicionada é **nulo** (não atribuído) após esta operação.</span><span class="sxs-lookup"><span data-stu-id="a4132-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="a4132-108">Para definir ou alterar o valor de uma propriedade WMI, você deve definir a propriedade [**Value**](swbemdatetime-value.md) do objeto [**SWbemProperty**](swbemproperty.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="a4132-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="a4132-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a4132-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4132-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4132-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a4132-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4132-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4132-112">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4132-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4132-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a4132-113">Required.</span></span> <span data-ttu-id="a4132-114">Nome da nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="a4132-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="a4132-115">*iCIMType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4132-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4132-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a4132-116">Required.</span></span> <span data-ttu-id="a4132-117">Um inteiro que representa o qualificador **CIMType** da nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="a4132-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="a4132-118">Consulte [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) para obter a lista com os qualificadores **CIMType** e seus valores.</span><span class="sxs-lookup"><span data-stu-id="a4132-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="a4132-119">*bIsArray* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a4132-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4132-120">Especifica se a propriedade é um tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="a4132-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="a4132-121">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="a4132-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a4132-122">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a4132-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4132-123">Reservado e deve ser zero se especificado.</span><span class="sxs-lookup"><span data-stu-id="a4132-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4132-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4132-124">Return value</span></span>

<span data-ttu-id="a4132-125">Se for bem-sucedido, esse método retornará um objeto [**SWbemProperty**](swbemproperty.md) que representa a nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="a4132-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="a4132-126">Caso contrário, um objeto **nulo** será retornado.</span><span class="sxs-lookup"><span data-stu-id="a4132-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a4132-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a4132-127">Error codes</span></span>

<span data-ttu-id="a4132-128">Após a conclusão do método **Add** , o objeto **Err** pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="a4132-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="a4132-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a4132-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a4132-130">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="a4132-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a4132-131">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a4132-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a4132-132">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a4132-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="a4132-133">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a4132-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a4132-134">Não há memória suficiente para execução deste método.</span><span class="sxs-lookup"><span data-stu-id="a4132-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="a4132-135">**wbemErrInvalidPropertyType** -2147749930</span><span class="sxs-lookup"><span data-stu-id="a4132-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="a4132-136">O qualificador **CIMType** não é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="a4132-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a4132-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4132-137">Examples</span></span>

<span data-ttu-id="a4132-138">Para obter um exemplo de código que usa esse método, consulte o tópico [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="a4132-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4132-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4132-139">Requirements</span></span>



| <span data-ttu-id="a4132-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4132-140">Requirement</span></span> | <span data-ttu-id="a4132-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a4132-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4132-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4132-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a4132-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4132-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4132-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4132-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a4132-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4132-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4132-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4132-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4132-147"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4132-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4132-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a4132-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4132-149"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4132-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4132-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a4132-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4132-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4132-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4132-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="a4132-152">CLSID</span></span><br/>                    | <span data-ttu-id="a4132-153">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="a4132-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="a4132-154">IID</span><span class="sxs-lookup"><span data-stu-id="a4132-154">IID</span></span><br/>                      | <span data-ttu-id="a4132-155">ISWbemPropertySet de IID \_</span><span class="sxs-lookup"><span data-stu-id="a4132-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="a4132-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4132-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4132-157">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a4132-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="a4132-158">**SWbemPropertySet. Remove**</span><span class="sxs-lookup"><span data-stu-id="a4132-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="a4132-159">**SWbemProperty. Value**</span><span class="sxs-lookup"><span data-stu-id="a4132-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




