---
description: Compara duas cadeias de caracteres Unicode, usando uma localidade especificada.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Função CompareStringWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967358"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="f9022-103">Função CompareStringWrapW</span><span class="sxs-lookup"><span data-stu-id="f9022-103">CompareStringWrapW function</span></span>

<span data-ttu-id="f9022-104">\[O **CompareStringWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9022-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="f9022-105">Ele não estará disponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f9022-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="f9022-106">Você deve usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="f9022-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="f9022-107">Compara duas cadeias de caracteres Unicode, usando uma localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="f9022-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="f9022-108">**CompareStringWrapW** é um wrapper para a função **CompareStringW** .</span><span class="sxs-lookup"><span data-stu-id="f9022-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="f9022-109">Consulte a página [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="f9022-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f9022-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9022-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="f9022-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9022-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9022-112">*Localidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f9022-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9022-113">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="f9022-113">Type: **LCID**</span></span>

<span data-ttu-id="f9022-114">Um identificador de localidade usado para a comparação.</span><span class="sxs-lookup"><span data-stu-id="f9022-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="f9022-115">Esse parâmetro pode ser um dos seguintes identificadores de localidade predefinidos ou um identificador de localidade criado pela macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="f9022-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="f9022-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**\_padrão do sistema de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="f9022-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-117">A localidade padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="f9022-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="f9022-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_padrão de usuário de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="f9022-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-119">A localidade padrão do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f9022-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f9022-120">*dwCmpFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9022-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9022-121">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f9022-121">Type: **DWORD**</span></span>

<span data-ttu-id="f9022-122">Os sinalizadores que indicam como a função compara as duas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9022-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="f9022-123">Por padrão, esses sinalizadores não são definidos.</span><span class="sxs-lookup"><span data-stu-id="f9022-123">By default, these flags are not set.</span></span> <span data-ttu-id="f9022-124">Defina como zero para obter o comportamento padrão ou para qualquer combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9022-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="f9022-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**IGNORECASE de normal \_**</span><span class="sxs-lookup"><span data-stu-id="f9022-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-126">Ignorar maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9022-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="f9022-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**\_IGNOREKANATYPE normal**</span><span class="sxs-lookup"><span data-stu-id="f9022-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-128">Não diferenciar entre caracteres hiragana e Katakana.</span><span class="sxs-lookup"><span data-stu-id="f9022-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="f9022-129">Os caracteres hiragana e katakana correspondentes são comparados como iguais.</span><span class="sxs-lookup"><span data-stu-id="f9022-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="f9022-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**\_IGNORENONSPACE normal**</span><span class="sxs-lookup"><span data-stu-id="f9022-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-131">Ignorar caracteres de não espaçamento.</span><span class="sxs-lookup"><span data-stu-id="f9022-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="f9022-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**\_IGNORESYMBOLS normal**</span><span class="sxs-lookup"><span data-stu-id="f9022-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-133">Ignorar símbolos.</span><span class="sxs-lookup"><span data-stu-id="f9022-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="f9022-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**\_IGNOREWIDTH normal**</span><span class="sxs-lookup"><span data-stu-id="f9022-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-135">Não Diferencie entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="f9022-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="f9022-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**CLASSIFICAR \_ STRINGSORT**</span><span class="sxs-lookup"><span data-stu-id="f9022-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="f9022-137">Trate a pontuação da mesma forma que os símbolos.</span><span class="sxs-lookup"><span data-stu-id="f9022-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f9022-138">*lpString1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9022-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9022-139">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f9022-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="f9022-140">Um ponteiro para a primeira cadeia de caracteres Unicode a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="f9022-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="f9022-141">*cchCount1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9022-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9022-142">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f9022-142">Type: **int**</span></span>

<span data-ttu-id="f9022-143">O número de caracteres na cadeia de caracteres apontada pelo parâmetro *lpString1* .</span><span class="sxs-lookup"><span data-stu-id="f9022-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="f9022-144">A contagem não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="f9022-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="f9022-145">Se esse parâmetro for um valor negativo, a cadeia de caracteres será considerada como terminada em nulo e o comprimento será calculado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f9022-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="f9022-146">*lpString2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9022-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9022-147">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f9022-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="f9022-148">Um ponteiro para a segunda cadeia de caracteres Unicode a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="f9022-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="f9022-149">*cchCount2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9022-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9022-150">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f9022-150">Type: **int**</span></span>

<span data-ttu-id="f9022-151">O número de caracteres na cadeia de caracteres apontada pelo parâmetro *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="f9022-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="f9022-152">A contagem não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="f9022-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="f9022-153">Se esse parâmetro for um valor negativo, a cadeia de caracteres será considerada como terminada em nulo e o comprimento será calculado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f9022-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9022-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9022-154">Return value</span></span>

<span data-ttu-id="f9022-155">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f9022-155">Type: **int**</span></span>

<span data-ttu-id="f9022-156">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="f9022-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="f9022-157">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="f9022-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="f9022-158">**GetLastError** pode retornar um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="f9022-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="f9022-159">\_Sinalizadores inválidos de erro \_</span><span class="sxs-lookup"><span data-stu-id="f9022-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="f9022-160">\_parâmetro inválido de erro \_</span><span class="sxs-lookup"><span data-stu-id="f9022-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="f9022-161">Se a função for realizada com sucesso, o valor de retorno será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9022-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="f9022-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9022-162">Requirement</span></span> | <span data-ttu-id="f9022-163">Valor</span><span class="sxs-lookup"><span data-stu-id="f9022-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9022-164">CSTR \_ menor \_ que</span><span class="sxs-lookup"><span data-stu-id="f9022-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="f9022-165">A cadeia de caracteres apontada pelo parâmetro *lpString1* é menos no valor léxico do que a cadeia de caracteres apontada pelo parâmetro *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="f9022-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="f9022-166">CSTR \_ igual</span><span class="sxs-lookup"><span data-stu-id="f9022-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="f9022-167">A cadeia de caracteres apontada por *lpString1* é igual no valor léxico à cadeia de caracteres apontada por *lpString2*.</span><span class="sxs-lookup"><span data-stu-id="f9022-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="f9022-168">CSTR \_ maior \_ que</span><span class="sxs-lookup"><span data-stu-id="f9022-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="f9022-169">A cadeia de caracteres apontada por *lpString1* é maior no valor léxico do que a cadeia de caracteres apontada por *lpString2*</span><span class="sxs-lookup"><span data-stu-id="f9022-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="f9022-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9022-170">Remarks</span></span>

<span data-ttu-id="f9022-171">**Aviso de segurança:** Usar essa função incorretamente pode comprometer a segurança do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9022-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="f9022-172">As cadeias de caracteres que não são comparadas corretamente podem produzir entradas inválidas.</span><span class="sxs-lookup"><span data-stu-id="f9022-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="f9022-173">Testar cadeias de caracteres para certificar-se de que elas são válidas antes de usá-las e fornecer manipuladores de erro.</span><span class="sxs-lookup"><span data-stu-id="f9022-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="f9022-174">Para obter mais informações, consulte [considerações de segurança: recursos internacionais](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="f9022-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="f9022-175">O método preferencial é usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="f9022-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="f9022-176">**CompareStringWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 45.</span><span class="sxs-lookup"><span data-stu-id="f9022-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9022-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9022-177">Requirements</span></span>



| <span data-ttu-id="f9022-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9022-178">Requirement</span></span> | <span data-ttu-id="f9022-179">Valor</span><span class="sxs-lookup"><span data-stu-id="f9022-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9022-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9022-180">Minimum supported client</span></span><br/> | <span data-ttu-id="f9022-181">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9022-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9022-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9022-182">Minimum supported server</span></span><br/> | <span data-ttu-id="f9022-183">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9022-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f9022-184">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9022-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9022-185"><dt>Nenhum</dt></span><span class="sxs-lookup"><span data-stu-id="f9022-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="f9022-186">DLL</span><span class="sxs-lookup"><span data-stu-id="f9022-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9022-187"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f9022-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9022-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9022-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9022-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="f9022-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
