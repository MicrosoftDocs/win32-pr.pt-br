---
description: Fornece uma lista de scripts para a localidade especificada.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Função DownlevelGetLocaleScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171294"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="580c5-103">Função DownlevelGetLocaleScripts</span><span class="sxs-lookup"><span data-stu-id="580c5-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="580c5-104">Fornece uma lista de scripts para a localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="580c5-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="580c5-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="580c5-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="580c5-106">Seu uso requer o pacote de download.</span><span class="sxs-lookup"><span data-stu-id="580c5-106">Its use requires the download package.</span></span> <span data-ttu-id="580c5-107">Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCTYPE* definido como [localidade \_ SSCRIPTS](locale-sscripts.md).</span><span class="sxs-lookup"><span data-stu-id="580c5-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="580c5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="580c5-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="580c5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="580c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="580c5-110">*lpLocaleName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="580c5-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580c5-111">Ponteiro para um [nome de localidade](locale-names.md)terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="580c5-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="580c5-112">*lpScripts* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="580c5-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="580c5-113">Ponteiro para um buffer no qual essa função recupera uma cadeia de caracteres terminada em nulo que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="580c5-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="580c5-114">Cada nome de script consiste em quatro caracteres latinos, e os nomes são recuperados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="580c5-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="580c5-115">Cada um deles, incluindo o último, é seguido por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="580c5-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="580c5-116">Como alternativa, esse parâmetro pode conter **NULL** se *cchScripts* for definido como 0.</span><span class="sxs-lookup"><span data-stu-id="580c5-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="580c5-117">Nesse caso, a função retorna o tamanho necessário para o buffer de script.</span><span class="sxs-lookup"><span data-stu-id="580c5-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="580c5-118">*cchScripts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="580c5-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580c5-119">Tamanho, em caracteres, para o buffer de script indicado por *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="580c5-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="580c5-120">Como alternativa, o aplicativo pode definir esse parâmetro como 0.</span><span class="sxs-lookup"><span data-stu-id="580c5-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="580c5-121">Nesse caso, a função recupera **NULL** em *lpScripts* e retorna o tamanho necessário para o buffer de script.</span><span class="sxs-lookup"><span data-stu-id="580c5-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="580c5-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="580c5-122">Return value</span></span>

<span data-ttu-id="580c5-123">Retorna o número de caracteres recuperados no buffer de script, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="580c5-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="580c5-124">Se a função for bem sucedido e o valor de *cchScripts* for 0, o valor de retorno será o tamanho necessário, em caracteres, incluindo um caractere nulo de terminação, para o buffer de script.</span><span class="sxs-lookup"><span data-stu-id="580c5-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="580c5-125">Essa função retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="580c5-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="580c5-126">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="580c5-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="580c5-127">ERRO \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="580c5-127">ERROR\_BADDB.</span></span> <span data-ttu-id="580c5-128">A função não pôde acessar os dados.</span><span class="sxs-lookup"><span data-stu-id="580c5-128">The function could not access the data.</span></span> <span data-ttu-id="580c5-129">Essa situação normalmente não deve ocorrer e, normalmente, indica uma instalação inválida, um problema de disco ou assim por diante.</span><span class="sxs-lookup"><span data-stu-id="580c5-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="580c5-130">ERRO \_ de \_ buffer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="580c5-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="580c5-131">Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="580c5-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="580c5-132">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="580c5-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="580c5-133">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="580c5-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="580c5-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="580c5-134">Remarks</span></span>

<span data-ttu-id="580c5-135">Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="580c5-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="580c5-136">Aqui estão alguns exemplos de entradas e saídas para essa função, supondo um tamanho de buffer suficiente:</span><span class="sxs-lookup"><span data-stu-id="580c5-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="580c5-137">Locale</span><span class="sxs-lookup"><span data-stu-id="580c5-137">Locale</span></span>                  | <span data-ttu-id="580c5-138">*lpLocaleName*</span><span class="sxs-lookup"><span data-stu-id="580c5-138">*lpLocaleName*</span></span> | <span data-ttu-id="580c5-139">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="580c5-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="580c5-140">Inglês (Estados Unidos)</span><span class="sxs-lookup"><span data-stu-id="580c5-140">English (United States)</span></span> | <span data-ttu-id="580c5-141">pt-BR</span><span class="sxs-lookup"><span data-stu-id="580c5-141">en-US</span></span>          | <span data-ttu-id="580c5-142">Latn</span><span class="sxs-lookup"><span data-stu-id="580c5-142">Latn;</span></span>           |
| <span data-ttu-id="580c5-143">Híndi (Índia)</span><span class="sxs-lookup"><span data-stu-id="580c5-143">Hindi (India)</span></span>           | <span data-ttu-id="580c5-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="580c5-144">hi-IN</span></span>          | <span data-ttu-id="580c5-145">DESVPADPA</span><span class="sxs-lookup"><span data-stu-id="580c5-145">Deva;</span></span>           |
| <span data-ttu-id="580c5-146">Japonês (Japão)</span><span class="sxs-lookup"><span data-stu-id="580c5-146">Japanese (Japan)</span></span>        | <span data-ttu-id="580c5-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="580c5-147">ja-JP</span></span>          | <span data-ttu-id="580c5-148">Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="580c5-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="580c5-149">A lista não contém o script latino, a menos que seja uma parte essencial do sistema de escrita usado para uma localidade.</span><span class="sxs-lookup"><span data-stu-id="580c5-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="580c5-150">No entanto, os caracteres latinos são geralmente usados no contexto de localidades para os quais não são nativos, como para um nome comercial estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="580c5-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="580c5-151">No exemplo acima para Hindi na Índia, o único script recuperado é "DESVPADA" (para o Devanágari), embora os caracteres latinos também possam aparecer em texto em Híndi.</span><span class="sxs-lookup"><span data-stu-id="580c5-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="580c5-152">A função [**DownlevelVerifyScripts**](downlevelverifyscripts.md) tem um sinalizador especial para resolver esse caso.</span><span class="sxs-lookup"><span data-stu-id="580c5-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="580c5-153">O arquivo de cabeçalho e a DLL necessários fazem parte do download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="580c5-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="580c5-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="580c5-154">Requirements</span></span>



| <span data-ttu-id="580c5-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="580c5-155">Requirement</span></span> | <span data-ttu-id="580c5-156">Valor</span><span class="sxs-lookup"><span data-stu-id="580c5-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="580c5-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="580c5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="580c5-158">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="580c5-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="580c5-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="580c5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="580c5-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="580c5-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="580c5-161">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="580c5-161">Redistributable</span></span><br/>          | <span data-ttu-id="580c5-162">APIs de mitigação do IDN (Microsoft internacionalizated Domain Name) no Windows XP (SP2 ou posterior), Windows Server 2003 (SP1 ou posterior) ou Windows Vista</span><span class="sxs-lookup"><span data-stu-id="580c5-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="580c5-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="580c5-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="580c5-164"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="580c5-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="580c5-165">DLL</span><span class="sxs-lookup"><span data-stu-id="580c5-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="580c5-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="580c5-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="580c5-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="580c5-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580c5-168">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="580c5-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="580c5-169">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="580c5-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="580c5-170">Tratando IDNs (nomes de domínio internacionalizados)</span><span class="sxs-lookup"><span data-stu-id="580c5-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="580c5-171">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="580c5-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="580c5-172">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="580c5-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="580c5-173">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="580c5-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
