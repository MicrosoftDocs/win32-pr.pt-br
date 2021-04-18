---
description: Fornece uma lista de scripts usados na cadeia de caracteres Unicode especificada.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Função DownlevelGetStringScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792510"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="df495-103">Função DownlevelGetStringScripts</span><span class="sxs-lookup"><span data-stu-id="df495-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="df495-104">Fornece uma lista de scripts usados na cadeia de caracteres Unicode especificada.</span><span class="sxs-lookup"><span data-stu-id="df495-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="df495-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df495-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="df495-106">Seu uso requer o pacote de download.</span><span class="sxs-lookup"><span data-stu-id="df495-106">Its use requires the download package.</span></span> <span data-ttu-id="df495-107">Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span><span class="sxs-lookup"><span data-stu-id="df495-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="df495-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df495-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="df495-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df495-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df495-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df495-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df495-111">Sinalizadores que especificam opções para recuperação de script.</span><span class="sxs-lookup"><span data-stu-id="df495-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="df495-112">Valor</span><span class="sxs-lookup"><span data-stu-id="df495-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="df495-113">Significado</span><span class="sxs-lookup"><span data-stu-id="df495-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="df495-114"><dt>**GSS \_ permitir \_ herdado \_ comum**</dt></span><span class="sxs-lookup"><span data-stu-id="df495-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="df495-115">Recupere as informações de script "Qaii" (HERDAdo) e "Zyyy" (comum).</span><span class="sxs-lookup"><span data-stu-id="df495-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="df495-116">Esse valor não afeta o processamento de caracteres não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="df495-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="df495-117">Esses caracteres na cadeia de caracteres de entrada sempre fazem com que um "ZZZZ" (script não atribuído) apareça na cadeia de caracteres do script.</span><span class="sxs-lookup"><span data-stu-id="df495-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="df495-118">Por padrão, essa função ignora todos os caracteres herdados ou comuns na cadeia de caracteres Unicode de entrada.</span><span class="sxs-lookup"><span data-stu-id="df495-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="df495-119">Se GSS \_ permitir \_ herdado \_ comum não estiver definido, nem "Qaii" nem "Zyyy" aparecerão na cadeia de caracteres de script, mesmo que a cadeia de caracteres de entrada contenha esses caracteres.</span><span class="sxs-lookup"><span data-stu-id="df495-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="df495-120">Se GSS \_ permitir \_ herdado \_ comum estiver definido, e se a cadeia de caracteres de entrada contiver caracteres herdados e/ou comuns, "Qaii" e/ou "Zyyy" aparecerão na cadeia de caracteres do script.</span><span class="sxs-lookup"><span data-stu-id="df495-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="df495-121">Consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="df495-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="df495-122">*LPSTR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df495-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df495-123">Ponteiro para a cadeia de caracteres Unicode a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="df495-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="df495-124">*cchString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df495-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df495-125">Tamanho, em caracteres, da cadeia de caracteres Unicode indicada por *LPSTR*.</span><span class="sxs-lookup"><span data-stu-id="df495-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="df495-126">O aplicativo definirá esse parâmetro como-1 se a cadeia de caracteres for terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="df495-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="df495-127">Se o aplicativo definir esse parâmetro como 0, a função recuperará uma cadeia de caracteres Unicode nula (L " \\ 0") em *lpScripts* e retornará 1.</span><span class="sxs-lookup"><span data-stu-id="df495-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="df495-128">*lpScripts* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df495-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df495-129">Ponteiro para um buffer no qual essa função recupera uma cadeia de caracteres terminada em nulo que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="df495-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="df495-130">Cada nome de script consiste em quatro caracteres latinos, e os nomes são recuperados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="df495-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="df495-131">Cada nome, incluindo o último, é seguido por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="df495-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="df495-132">Como alternativa, esse parâmetro pode conter **NULL** se *cchScripts* definido como 0.</span><span class="sxs-lookup"><span data-stu-id="df495-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="df495-133">Nesse caso, a função retorna o tamanho necessário para o buffer de script.</span><span class="sxs-lookup"><span data-stu-id="df495-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="df495-134">*cchScripts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df495-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df495-135">Tamanho, em caracteres, para o buffer de script indicado por *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="df495-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="df495-136">Como alternativa, o aplicativo pode definir esse parâmetro como 0.</span><span class="sxs-lookup"><span data-stu-id="df495-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="df495-137">Nesse caso, a função recupera **NULL** em *lpScripts* e retorna o tamanho necessário para o buffer de script.</span><span class="sxs-lookup"><span data-stu-id="df495-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df495-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df495-138">Return value</span></span>

<span data-ttu-id="df495-139">Retorna o número de caracteres recuperados no buffer de saída, incluindo um caractere nulo de terminação, se bem-sucedido e *cchScripts* é definido como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="df495-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="df495-140">A função retorna 1 para indicar que nenhum script foi encontrado, por exemplo, quando a cadeia de caracteres de entrada contém apenas caracteres comuns ou HERDAdos e GSS \_ permitir \_ herdado \_ comum não está definido.</span><span class="sxs-lookup"><span data-stu-id="df495-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="df495-141">Considerando que cada script encontrado adiciona cinco caracteres (quatro caracteres + delimitador), uma operação matemática simples fornece a contagem de script como ( \_ código de retorno-1)/5.</span><span class="sxs-lookup"><span data-stu-id="df495-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="df495-142">Se a função for bem sucedido e o valor de *cchScripts* for 0, o valor de retorno será o tamanho necessário, em caracteres, incluindo um caractere nulo de terminação, para o buffer de script.</span><span class="sxs-lookup"><span data-stu-id="df495-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="df495-143">A contagem de script é conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="df495-143">The script count is as described above.</span></span>

<span data-ttu-id="df495-144">A função retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="df495-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="df495-145">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="df495-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="df495-146">ERRO \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="df495-146">ERROR\_BADDB.</span></span> <span data-ttu-id="df495-147">A função não pôde acessar os dados.</span><span class="sxs-lookup"><span data-stu-id="df495-147">The function could not access the data.</span></span> <span data-ttu-id="df495-148">Essa situação normalmente não deve ocorrer e, normalmente, indica uma instalação inválida, um problema de disco ou assim por diante.</span><span class="sxs-lookup"><span data-stu-id="df495-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="df495-149">ERRO \_ de \_ buffer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="df495-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="df495-150">Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="df495-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="df495-151">ERROS de \_ Sinalizadores inválidos \_ .</span><span class="sxs-lookup"><span data-stu-id="df495-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="df495-152">Os valores fornecidos para sinalizadores não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="df495-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="df495-153">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="df495-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="df495-154">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="df495-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="df495-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="df495-155">Remarks</span></span>

<span data-ttu-id="df495-156">Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="df495-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="df495-157">A determinação do script é baseada nos valores de script publicados pelo consórcio Unicode no <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , exceto pelo fato de que os caracteres não atribuídos têm o valor "ZZZZ" (não atribuído) em vez de "Zyyy" (comum).</span><span class="sxs-lookup"><span data-stu-id="df495-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="df495-158">Aqui estão alguns exemplos do comportamento dessa função:</span><span class="sxs-lookup"><span data-stu-id="df495-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="df495-159">Cadeia de caracteres de entrada</span><span class="sxs-lookup"><span data-stu-id="df495-159">Input string</span></span>

<span data-ttu-id="df495-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="df495-160">*dwFlags*</span></span>

<span data-ttu-id="df495-161">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="df495-161">*lpScripts*</span></span>

<span data-ttu-id="df495-162">Scripts</span><span class="sxs-lookup"><span data-stu-id="df495-162">Scripts</span></span>

<span data-ttu-id="df495-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="df495-163">Microsoft.com</span></span>

<span data-ttu-id="df495-164">0</span><span class="sxs-lookup"><span data-stu-id="df495-164">0</span></span>

<span data-ttu-id="df495-165">Latn</span><span class="sxs-lookup"><span data-stu-id="df495-165">Latn;</span></span>

<span data-ttu-id="df495-166">Latim</span><span class="sxs-lookup"><span data-stu-id="df495-166">Latin</span></span>

<span data-ttu-id="df495-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="df495-167">Microsoft.com</span></span>

<span data-ttu-id="df495-168">GSS \_ permitir \_ herdado \_ comum</span><span class="sxs-lookup"><span data-stu-id="df495-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="df495-169">Latn Zyyy;</span><span class="sxs-lookup"><span data-stu-id="df495-169">Latn;Zyyy;</span></span>

<span data-ttu-id="df495-170">Latino + comum</span><span class="sxs-lookup"><span data-stu-id="df495-170">Latin + Common</span></span>

<span data-ttu-id="df495-171">$ {ROWSPAN2} $Ni ño $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="df495-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="df495-172">004E 0069 0241 006F</span><span class="sxs-lookup"><span data-stu-id="df495-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="df495-173">$ {ROWSPAN2} $GSS \_ permitir \_ herdado \_ $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="df495-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="df495-174">$ {ROWSPAN2} $Latn; $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="df495-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="df495-175">$ {ROWSPAN2} $Latin $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="df495-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="df495-176">Usa letra latina minúscula N com til</span><span class="sxs-lookup"><span data-stu-id="df495-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="df495-177">$ {ROWSPAN2} $Ni ño $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="df495-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="df495-178">004E 0069 006E 0303 006F</span><span class="sxs-lookup"><span data-stu-id="df495-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="df495-179">$ {ROWSPAN2} $GSS \_ permitir \_ herdado \_ $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="df495-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="df495-180">$ {ROWSPAN2} $Latn; Qaii; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="df495-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="df495-181">$ {ROWSPAN2} $Latin + herdado $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="df495-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="df495-182">Usa til COMBINÁvel</span><span class="sxs-lookup"><span data-stu-id="df495-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="df495-183">$ {ROWSPAN2} $Sp ооf $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="df495-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="df495-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="df495-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="df495-185">$ {ROWSPAN2} $0 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="df495-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="df495-186">$ {ROWSPAN2} $Latn; Cyrl; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="df495-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="df495-187">$ {ROWSPAN2} $Latin + cirílico $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="df495-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="df495-188">Usa letra CIRÍLICA minúscula O</span><span class="sxs-lookup"><span data-stu-id="df495-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="df495-189"></span><span class="sxs-lookup"><span data-stu-id="df495-189"></span></span>

<span data-ttu-id="df495-190">U + F000</span><span class="sxs-lookup"><span data-stu-id="df495-190">U+f000</span></span>

<span data-ttu-id="df495-191">0</span><span class="sxs-lookup"><span data-stu-id="df495-191">0</span></span>

<span data-ttu-id="df495-192">Zzzz;</span><span class="sxs-lookup"><span data-stu-id="df495-192">Zzzz;</span></span>

<span data-ttu-id="df495-193">Não atribuído</span><span class="sxs-lookup"><span data-stu-id="df495-193">Unassigned</span></span>

<span data-ttu-id="df495-194"></span><span class="sxs-lookup"><span data-stu-id="df495-194"></span></span>

<span data-ttu-id="df495-195">U + F000</span><span class="sxs-lookup"><span data-stu-id="df495-195">U+f000</span></span>

<span data-ttu-id="df495-196">GSS \_ permitir \_ herdado \_ comum</span><span class="sxs-lookup"><span data-stu-id="df495-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="df495-197">Zzzz;</span><span class="sxs-lookup"><span data-stu-id="df495-197">Zzzz;</span></span>

<span data-ttu-id="df495-198">Não atribuído</span><span class="sxs-lookup"><span data-stu-id="df495-198">Unassigned</span></span>



 

<span data-ttu-id="df495-199">O arquivo de cabeçalho e a DLL necessários fazem parte do download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="df495-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="df495-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df495-200">Requirements</span></span>



| <span data-ttu-id="df495-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="df495-201">Requirement</span></span> | <span data-ttu-id="df495-202">Valor</span><span class="sxs-lookup"><span data-stu-id="df495-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df495-203">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df495-203">Minimum supported client</span></span><br/> | <span data-ttu-id="df495-204">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="df495-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="df495-205">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df495-205">Minimum supported server</span></span><br/> | <span data-ttu-id="df495-206">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df495-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="df495-207">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="df495-207">Redistributable</span></span><br/>          | <span data-ttu-id="df495-208">APIs de mitigação do IDN (Microsoft internacionalizated Domain Name) no Windows XP (SP2 ou posterior), Windows Server 2003 (SP1 ou posterior) ou Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df495-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="df495-209">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df495-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="df495-210"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df495-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="df495-211">DLL</span><span class="sxs-lookup"><span data-stu-id="df495-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df495-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df495-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="df495-213">Confira também</span><span class="sxs-lookup"><span data-stu-id="df495-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df495-214">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="df495-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="df495-215">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="df495-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="df495-216">Tratando IDNs (nomes de domínio internacionalizados)</span><span class="sxs-lookup"><span data-stu-id="df495-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="df495-217">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="df495-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="df495-218">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="df495-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="df495-219">**GetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="df495-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
