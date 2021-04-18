---
description: Compara duas listas enumeradas de scripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Função DownlevelVerifyScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756916"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="a2ea2-103">Função DownlevelVerifyScripts</span><span class="sxs-lookup"><span data-stu-id="a2ea2-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="a2ea2-104">Compara duas listas enumeradas de scripts.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="a2ea2-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="a2ea2-106">Seu uso requer o pacote de download.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-106">Its use requires the download package.</span></span> <span data-ttu-id="a2ea2-107">Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span><span class="sxs-lookup"><span data-stu-id="a2ea2-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a2ea2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2ea2-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="a2ea2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2ea2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ea2-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea2-111">Sinalizadores que especificam opções de verificação de script.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="a2ea2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ea2-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="a2ea2-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a2ea2-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="a2ea2-114"><dt>**VS \_ permitir \_ latino**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ea2-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="a2ea2-115">Permitir "Latn" (script latino) na lista de testes, mesmo se não estiver na lista de localidade.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2ea2-116">*lpLocaleScripts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea2-117">Aponta para a lista de localidade, a lista enumerada de scripts para uma determinada localidade.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="a2ea2-118">Normalmente, essa lista é preenchida chamando [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span><span class="sxs-lookup"><span data-stu-id="a2ea2-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2ea2-119">*cchLocaleScripts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea2-120">Tamanho, em caracteres, da cadeia de caracteres indicada por *lpLocaleScripts*.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="a2ea2-121">O aplicativo definirá esse parâmetro como-1 se a cadeia de caracteres for terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="a2ea2-122">Se esse parâmetro for definido como 0, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="a2ea2-123">*lpTestScripts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea2-124">Ponteiro para a lista de testes, uma segunda lista enumerada de scripts.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="a2ea2-125">Normalmente, essa lista é preenchida chamando [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span><span class="sxs-lookup"><span data-stu-id="a2ea2-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2ea2-126">*cchTestScripts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea2-127">Tamanho, em caracteres, da cadeia de caracteres indicada por *lpTestScripts*.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="a2ea2-128">O aplicativo definirá esse parâmetro como-1 se a cadeia de caracteres for terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="a2ea2-129">Se esse parâmetro for definido como 0, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ea2-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2ea2-130">Return value</span></span>

<span data-ttu-id="a2ea2-131">Retornará **true** se a lista de testes não estiver vazia e todos os itens da lista também estiverem incluídos na lista de localidade.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="a2ea2-132">Caso contrário, a função retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="a2ea2-133">Um valor de retorno **false** pode indicar que a lista de testes contém um item que não está na lista de localidade ou pode indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="a2ea2-134">Para distinguir entre esses dois casos, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a2ea2-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="a2ea2-135">Se **DownlevelVerifyScripts** tiver determinado com êxito que há um item na lista de testes que não está na lista de localidade, **GetLastError** retornará o êxito do erro \_ .</span><span class="sxs-lookup"><span data-stu-id="a2ea2-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="a2ea2-136">Caso contrário, **GetLastError** pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="a2ea2-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="a2ea2-137">ERROS de \_ Sinalizadores inválidos \_ .</span><span class="sxs-lookup"><span data-stu-id="a2ea2-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="a2ea2-138">Os valores fornecidos para sinalizadores não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="a2ea2-139">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="a2ea2-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="a2ea2-140">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ea2-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2ea2-141">Remarks</span></span>

<span data-ttu-id="a2ea2-142">Essa função compara Cadeias de caracteres, como "Latn; Cyrl; ", que consiste em uma série de nomes de script de 4 caracteres, com cada nome de script seguido por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="a2ea2-143">Ele também tem um caso especial para considerar o fato de que o script Latin é geralmente usado em linguagens e localidades para as quais não é nativo.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="a2ea2-144">Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="a2ea2-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="a2ea2-145">Veja a seguir exemplos do retorno dessa função e uma chamada subsequente para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) em vários cenários.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="a2ea2-146">Os dois últimos exemplos ilustram, respectivamente, um caso em que a lista de testes não tem um ponto-e-vírgula de terminação (cadeia de caracteres malformada) e um caso em que a lista de testes está vazia.</span><span class="sxs-lookup"><span data-stu-id="a2ea2-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="a2ea2-147">Cadeia de caracteres "locale"</span><span class="sxs-lookup"><span data-stu-id="a2ea2-147">"Locale" string</span></span> | <span data-ttu-id="a2ea2-148">Cadeia de caracteres de "teste"</span><span class="sxs-lookup"><span data-stu-id="a2ea2-148">"Test" string</span></span> | <span data-ttu-id="a2ea2-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a2ea2-149">*dwFlags*</span></span>        | <span data-ttu-id="a2ea2-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2ea2-150">Return value</span></span> | <span data-ttu-id="a2ea2-151">Retorno de GetLastError</span><span class="sxs-lookup"><span data-stu-id="a2ea2-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="a2ea2-152">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="a2ea2-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="a2ea2-153">Hani;</span><span class="sxs-lookup"><span data-stu-id="a2ea2-153">Hani;</span></span>         | <span data-ttu-id="a2ea2-154">N/D</span><span class="sxs-lookup"><span data-stu-id="a2ea2-154">N/A</span></span>              | <span data-ttu-id="a2ea2-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-155">**TRUE**</span></span>     | <span data-ttu-id="a2ea2-156">N/D</span><span class="sxs-lookup"><span data-stu-id="a2ea2-156">N/A</span></span>                       |
| <span data-ttu-id="a2ea2-157">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="a2ea2-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="a2ea2-158">Hani; Latn</span><span class="sxs-lookup"><span data-stu-id="a2ea2-158">Hani;Latn;</span></span>    | <span data-ttu-id="a2ea2-159">0</span><span class="sxs-lookup"><span data-stu-id="a2ea2-159">0</span></span>                | <span data-ttu-id="a2ea2-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-160">**FALSE**</span></span>    | <span data-ttu-id="a2ea2-161">êxito do erro \_</span><span class="sxs-lookup"><span data-stu-id="a2ea2-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="a2ea2-162">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="a2ea2-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="a2ea2-163">Hani; Latn</span><span class="sxs-lookup"><span data-stu-id="a2ea2-163">Hani;Latn;</span></span>    | <span data-ttu-id="a2ea2-164">VS \_ permitir \_ latino</span><span class="sxs-lookup"><span data-stu-id="a2ea2-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="a2ea2-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-165">**TRUE**</span></span>     | <span data-ttu-id="a2ea2-166">N/D</span><span class="sxs-lookup"><span data-stu-id="a2ea2-166">N/A</span></span>                       |
| <span data-ttu-id="a2ea2-167">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="a2ea2-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="a2ea2-168">Cyrl;</span><span class="sxs-lookup"><span data-stu-id="a2ea2-168">Cyrl;</span></span>         | <span data-ttu-id="a2ea2-169">N/D</span><span class="sxs-lookup"><span data-stu-id="a2ea2-169">N/A</span></span>              | <span data-ttu-id="a2ea2-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-170">**FALSE**</span></span>    | <span data-ttu-id="a2ea2-171">êxito do erro \_</span><span class="sxs-lookup"><span data-stu-id="a2ea2-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="a2ea2-172">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="a2ea2-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="a2ea2-173">Cyrl;</span><span class="sxs-lookup"><span data-stu-id="a2ea2-173">Cyrl;</span></span>         | <span data-ttu-id="a2ea2-174">N/D</span><span class="sxs-lookup"><span data-stu-id="a2ea2-174">N/A</span></span>              | <span data-ttu-id="a2ea2-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-175">**FALSE**</span></span>    | <span data-ttu-id="a2ea2-176">\_parâmetro inválido de erro \_</span><span class="sxs-lookup"><span data-stu-id="a2ea2-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="a2ea2-177">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="a2ea2-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="a2ea2-178">N/D</span><span class="sxs-lookup"><span data-stu-id="a2ea2-178">N/A</span></span>              | <span data-ttu-id="a2ea2-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-179">**FALSE**</span></span>    | <span data-ttu-id="a2ea2-180">êxito do erro \_</span><span class="sxs-lookup"><span data-stu-id="a2ea2-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="a2ea2-181">O arquivo de cabeçalho e a DLL necessários fazem parte do download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="a2ea2-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ea2-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ea2-182">Requirements</span></span>



| <span data-ttu-id="a2ea2-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ea2-183">Requirement</span></span> | <span data-ttu-id="a2ea2-184">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ea2-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ea2-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2ea2-185">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ea2-186">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="a2ea2-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2ea2-187">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ea2-188">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2ea2-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="a2ea2-189">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a2ea2-189">Redistributable</span></span><br/>          | <span data-ttu-id="a2ea2-190">APIs de mitigação do IDN (nome de domínio internacionalizado) da Microsoft no Windows XP com SP2, Windows Server 2003 com SP1, orWindows vista</span><span class="sxs-lookup"><span data-stu-id="a2ea2-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="a2ea2-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2ea2-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ea2-192"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ea2-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="a2ea2-193">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ea2-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ea2-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ea2-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="a2ea2-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2ea2-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ea2-196">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="a2ea2-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="a2ea2-197">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="a2ea2-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="a2ea2-198">Tratando IDNs (nomes de domínio internacionalizados)</span><span class="sxs-lookup"><span data-stu-id="a2ea2-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="a2ea2-199">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="a2ea2-200">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="a2ea2-201">**VerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="a2ea2-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
