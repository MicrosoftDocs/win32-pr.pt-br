---
description: O \_ método CompareTo do objeto SWbemObject compara dois objetos SWbemObject. Essa comparação está sujeita a determinadas restrições com base nos valores especificados no parâmetro iFlags.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Método de SWbemObject.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661760"
---
# <a name="swbemobjectcompareto_-method"></a><span data-ttu-id="1f491-104">Método SWbemObject. CompareTo \_</span><span class="sxs-lookup"><span data-stu-id="1f491-104">SWbemObject.CompareTo\_ method</span></span>

<span data-ttu-id="1f491-105">O **método \_ CompareTo** do objeto [**SWbemObject**](swbemobject.md) compara dois objetos **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="1f491-105">The **CompareTo\_** method of the [**SWbemObject**](swbemobject.md) object compares two **SWbemObject** objects.</span></span> <span data-ttu-id="1f491-106">Essa comparação está sujeita a determinadas restrições com base nos valores especificados no parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="1f491-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="1f491-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1f491-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f491-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f491-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1f491-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f491-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f491-110">*objwbemObject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f491-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f491-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1f491-111">Required.</span></span> <span data-ttu-id="1f491-112">Esse parâmetro é um objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="1f491-112">This parameter is an [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="1f491-113">Esse é o objeto com o qual o primeiro objeto é comparado.</span><span class="sxs-lookup"><span data-stu-id="1f491-113">This is the object with which the first object is compared.</span></span> <span data-ttu-id="1f491-114">O objeto deve ser uma instância de **SWbemObject** válida.</span><span class="sxs-lookup"><span data-stu-id="1f491-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="1f491-115">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f491-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f491-116">Especifica as características do objeto a considerar ao comparar um objeto com outros objetos.</span><span class="sxs-lookup"><span data-stu-id="1f491-116">Specifies the object characteristics to consider when comparing an object with other objects.</span></span> <span data-ttu-id="1f491-117">Você pode usar **wbemComparisonFlagIncludeAll** para considerar todos os recursos (esse é o padrão) ou qualquer combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f491-117">You can use **wbemComparisonFlagIncludeAll** to consider all features (this is the default), or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="1f491-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1f491-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-119">Compara todas as propriedades, qualificadores e tipos.</span><span class="sxs-lookup"><span data-stu-id="1f491-119">Compares all properties, qualifiers, and flavors.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="1f491-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="1f491-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-121">Faz com que a origem dos objetos, ou seja, o servidor e o namespace do qual eles vieram, sejam ignorados em comparação com outros objetos.</span><span class="sxs-lookup"><span data-stu-id="1f491-121">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="1f491-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="1f491-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-123">Faz com que todos os qualificadores (incluindo a **chave** e **dinâmica**) sejam ignorados em comparação.</span><span class="sxs-lookup"><span data-stu-id="1f491-123">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="1f491-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="1f491-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-125">Faz com que valores padrão de propriedades sejam ignorados.</span><span class="sxs-lookup"><span data-stu-id="1f491-125">Causes default values of properties to be ignored.</span></span> <span data-ttu-id="1f491-126">Esse sinalizador só é significativo para comparar classes.</span><span class="sxs-lookup"><span data-stu-id="1f491-126">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="1f491-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1f491-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-128">Faz com que os tipos de qualificador sejam ignorados.</span><span class="sxs-lookup"><span data-stu-id="1f491-128">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="1f491-129">Esse sinalizador leva em conta os valores do qualificador, mas ignora as distinções de flavor, como regras de propagação e restrições de substituição.</span><span class="sxs-lookup"><span data-stu-id="1f491-129">This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="1f491-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1f491-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-131">Compara valores de cadeia de caracteres de maneira não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1f491-131">Compares string values in a case-insensitive manner.</span></span> <span data-ttu-id="1f491-132">Isso se aplica tanto a cadeias de caracteres quanto a valores de qualificador.</span><span class="sxs-lookup"><span data-stu-id="1f491-132">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="1f491-133">Nomes de propriedade e de qualificador sempre são comparados sem diferenciação de maiúsculas e minúsculas, seja este sinalizador especificado ou não.</span><span class="sxs-lookup"><span data-stu-id="1f491-133">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="1f491-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="1f491-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="1f491-135">Instrui o sistema a assumir que os objetos sendo comparados são instâncias da mesma classe.</span><span class="sxs-lookup"><span data-stu-id="1f491-135">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="1f491-136">Consequentemente, esse sinalizador compara apenas informações relacionadas à instância.</span><span class="sxs-lookup"><span data-stu-id="1f491-136">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="1f491-137">Use este sinalizador para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1f491-137">Use this flag to optimize performance.</span></span> <span data-ttu-id="1f491-138">Se os objetos não são da mesma classe, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1f491-138">If the objects are not of the same class, the results are undefined.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f491-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f491-139">Return value</span></span>

<span data-ttu-id="1f491-140">Esse método retornará o valor booliano de **true** se os objetos forem correspondentes.</span><span class="sxs-lookup"><span data-stu-id="1f491-140">This method returns the Boolean value of **TRUE** if the objects match.</span></span> <span data-ttu-id="1f491-141">Retornará **false** se os objetos não corresponderem.</span><span class="sxs-lookup"><span data-stu-id="1f491-141">It returns **FALSE** if the objects do not match.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f491-142">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1f491-142">Error codes</span></span>

<span data-ttu-id="1f491-143">Após a conclusão do método **CompareTo \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f491-143">After the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="1f491-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1f491-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1f491-145">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1f491-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1f491-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1f491-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1f491-147">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="1f491-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1f491-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="1f491-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1f491-149">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="1f491-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f491-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f491-150">Requirements</span></span>



| <span data-ttu-id="1f491-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f491-151">Requirement</span></span> | <span data-ttu-id="1f491-152">Valor</span><span class="sxs-lookup"><span data-stu-id="1f491-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f491-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f491-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1f491-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f491-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f491-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f491-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1f491-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f491-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f491-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f491-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f491-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f491-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f491-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1f491-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f491-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f491-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f491-161">DLL</span><span class="sxs-lookup"><span data-stu-id="1f491-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f491-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f491-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f491-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="1f491-163">CLSID</span></span><br/>                    | <span data-ttu-id="1f491-164">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="1f491-164">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="1f491-165">IID</span><span class="sxs-lookup"><span data-stu-id="1f491-165">IID</span></span><br/>                      | <span data-ttu-id="1f491-166">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="1f491-166">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="1f491-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f491-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f491-168">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="1f491-168">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




