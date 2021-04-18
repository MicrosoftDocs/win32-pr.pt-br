---
description: O \_ método CompareTo do objeto SWbemLastError compara dois objetos SWbemObject. Essa comparação está sujeita a determinadas restrições com base nos valores especificados no parâmetro iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Método de SWbemLastError.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771277"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="6ceed-104">Método SWbemLastError. CompareTo \_</span><span class="sxs-lookup"><span data-stu-id="6ceed-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="6ceed-105">O **método \_ CompareTo** do objeto [**SWbemLastError**](swbemlasterror.md) compara dois objetos [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="6ceed-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="6ceed-106">Essa comparação está sujeita a determinadas restrições com base nos valores especificados no parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="6ceed-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="6ceed-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6ceed-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ceed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ceed-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6ceed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ceed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ceed-110">*objwbemObject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ceed-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ceed-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="6ceed-111">Required.</span></span> <span data-ttu-id="6ceed-112">Um objeto de classe [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="6ceed-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="6ceed-113">Esse parâmetro é o objeto com o qual o primeiro objeto é comparado.</span><span class="sxs-lookup"><span data-stu-id="6ceed-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="6ceed-114">O objeto deve ser uma instância de **SWbemObject** válida.</span><span class="sxs-lookup"><span data-stu-id="6ceed-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="6ceed-115">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6ceed-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ceed-116">Um inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="6ceed-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="6ceed-117">Esse parâmetro especifica as características do objeto a serem consideradas quando comparações de objeto são feitas.</span><span class="sxs-lookup"><span data-stu-id="6ceed-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="6ceed-118">Você pode usar **wbemComparisonFlagIncludeAll** para considerar todos os recursos (padrão) ou qualquer combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ceed-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="6ceed-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6ceed-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-120">Faz com que todas as propriedades, qualificadores e tipos sejam comparados.</span><span class="sxs-lookup"><span data-stu-id="6ceed-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="6ceed-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="6ceed-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-122">Faz com que todos os qualificadores (incluindo a **chave** e **dinâmica**) sejam ignorados em comparação.</span><span class="sxs-lookup"><span data-stu-id="6ceed-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="6ceed-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="6ceed-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-124">Faz com que a origem dos objetos, ou seja, o servidor e o namespace do qual eles vieram, sejam ignorados em comparação com outros objetos.</span><span class="sxs-lookup"><span data-stu-id="6ceed-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="6ceed-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="6ceed-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-126">Faz com que os valores padrão das propriedades sejam ignorados.</span><span class="sxs-lookup"><span data-stu-id="6ceed-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="6ceed-127">Esse sinalizador só é significativo para comparar classes.</span><span class="sxs-lookup"><span data-stu-id="6ceed-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="6ceed-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="6ceed-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-129">Instrui o sistema a assumir que os objetos sendo comparados são instâncias da mesma classe.</span><span class="sxs-lookup"><span data-stu-id="6ceed-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="6ceed-130">Consequentemente, esse sinalizador compara apenas informações relacionadas à instância.</span><span class="sxs-lookup"><span data-stu-id="6ceed-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="6ceed-131">Use este sinalizador para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="6ceed-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="6ceed-132">Se os objetos não são da mesma classe, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="6ceed-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="6ceed-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="6ceed-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-134">Faz com que os valores de cadeia de caracteres sejam comparados de maneira não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6ceed-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="6ceed-135">Isso se aplica tanto a cadeias de caracteres quanto a valores de qualificador.</span><span class="sxs-lookup"><span data-stu-id="6ceed-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="6ceed-136">Nomes de propriedade e de qualificador sempre são comparados sem diferenciação de maiúsculas e minúsculas, seja este sinalizador especificado ou não.</span><span class="sxs-lookup"><span data-stu-id="6ceed-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="6ceed-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="6ceed-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="6ceed-138">Faz com que os tipos de qualificador sejam ignorados.</span><span class="sxs-lookup"><span data-stu-id="6ceed-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="6ceed-139">Este sinalizador ainda considera valores de qualificador, mas ignora diferenças de tipo como regras de propagação e restrições de substituição.</span><span class="sxs-lookup"><span data-stu-id="6ceed-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ceed-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ceed-140">Return value</span></span>

<span data-ttu-id="6ceed-141">O **método \_ CompareTo** retornará o valor booliano **true** se os objetos corresponderem; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="6ceed-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ceed-142">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6ceed-142">Error codes</span></span>

<span data-ttu-id="6ceed-143">Após a conclusão do método **CompareTo \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ceed-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6ceed-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6ceed-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6ceed-145">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6ceed-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6ceed-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6ceed-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6ceed-147">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="6ceed-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6ceed-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6ceed-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6ceed-149">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6ceed-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ceed-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ceed-150">Requirements</span></span>



| <span data-ttu-id="6ceed-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ceed-151">Requirement</span></span> | <span data-ttu-id="6ceed-152">Valor</span><span class="sxs-lookup"><span data-stu-id="6ceed-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ceed-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ceed-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6ceed-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ceed-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ceed-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ceed-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6ceed-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ceed-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ceed-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ceed-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ceed-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ceed-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ceed-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ceed-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ceed-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ceed-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ceed-161">DLL</span><span class="sxs-lookup"><span data-stu-id="6ceed-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ceed-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ceed-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ceed-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="6ceed-163">CLSID</span></span><br/>                    | <span data-ttu-id="6ceed-164">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="6ceed-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="6ceed-165">IID</span><span class="sxs-lookup"><span data-stu-id="6ceed-165">IID</span></span><br/>                      | <span data-ttu-id="6ceed-166">ISWbemLastError de IID \_</span><span class="sxs-lookup"><span data-stu-id="6ceed-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="6ceed-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ceed-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ceed-168">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="6ceed-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="6ceed-169">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="6ceed-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




