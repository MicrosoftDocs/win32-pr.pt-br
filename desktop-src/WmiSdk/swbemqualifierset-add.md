---
description: O método Add do objeto SWbemQualifierSet adiciona um objeto SWbemQualifier à coleção SWbemQualifierSet. Se já existir um qualificador com o mesmo nome na coleção, ele será substituído.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297489"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="4ccc1-104">Método SWbemQualifierSet. Add</span><span class="sxs-lookup"><span data-stu-id="4ccc1-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="4ccc1-105">O método **Add** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) adiciona um objeto [**SWbemQualifier**](swbemqualifier.md) à coleção **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="4ccc1-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="4ccc1-106">Se já existir um qualificador com o mesmo nome na coleção, ele será substituído.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="4ccc1-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4ccc1-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccc1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ccc1-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4ccc1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ccc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccc1-110">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ccc1-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-111">Required.</span></span> <span data-ttu-id="4ccc1-112">Nome do novo qualificador.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-113">*varVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ccc1-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-114">Required.</span></span> <span data-ttu-id="4ccc1-115">Valor da variante do novo qualificador.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-116">*bPropagatesToSubclasses* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ccc1-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-117">Valor booliano que indica se esse novo qualificador é propagado para subclasses.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="4ccc1-118">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-119">*bPropagatesToInstances* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ccc1-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-120">Valor booliano que indica se esse novo qualificador é propagado para instâncias.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="4ccc1-121">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-122">*bOverridable* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ccc1-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-123">Valor booliano que indica se este qualificador pode ser substituído quando propagado.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="4ccc1-124">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-125">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ccc1-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-126">Reserved.</span></span> <span data-ttu-id="4ccc1-127">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ccc1-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ccc1-128">Return value</span></span>

<span data-ttu-id="4ccc1-129">Se for bem-sucedido, esse método retornará um objeto [**SWbemQualifier**](swbemqualifier.md) que representa o novo qualificador.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="4ccc1-130">Caso contrário, um objeto **nulo** será retornado.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ccc1-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4ccc1-131">Error codes</span></span>

<span data-ttu-id="4ccc1-132">Após a conclusão do método **Add** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4ccc1-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4ccc1-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-134">O parâmetro *iFlags* não era válido.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-135">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4ccc1-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-136">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-137">**wbemErrCannotBeKey** -2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="4ccc1-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-138">Houve uma tentativa inválida de especificar um qualificador de **chave** em uma propriedade que não pode ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="4ccc1-139">As chaves são especificadas na definição de classe para um objeto e não podem ser alteradas por instância.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-140">**wbemErrInvalidQualifierType** -2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="4ccc1-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-141">O parâmetro *varVal* não é de um tipo de qualificador legal.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc1-142">**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="4ccc1-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="4ccc1-143">Não é possível executar a operação **SWbemQualifierSet. Add** neste qualificador porque o objeto proprietário não permite substituições.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ccc1-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ccc1-144">Requirements</span></span>



| <span data-ttu-id="4ccc1-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ccc1-145">Requirement</span></span> | <span data-ttu-id="4ccc1-146">Valor</span><span class="sxs-lookup"><span data-stu-id="4ccc1-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccc1-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ccc1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccc1-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ccc1-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ccc1-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ccc1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccc1-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ccc1-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ccc1-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ccc1-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ccc1-152"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ccc1-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ccc1-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ccc1-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ccc1-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4ccc1-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4ccc1-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4ccc1-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccc1-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ccc1-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ccc1-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="4ccc1-157">CLSID</span></span><br/>                    | <span data-ttu-id="4ccc1-158">\_SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="4ccc1-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="4ccc1-159">IID</span><span class="sxs-lookup"><span data-stu-id="4ccc1-159">IID</span></span><br/>                      | <span data-ttu-id="4ccc1-160">ISWbemQualifierSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="4ccc1-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="4ccc1-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ccc1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccc1-162">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="4ccc1-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="4ccc1-163">**SWbemQualifierSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="4ccc1-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




