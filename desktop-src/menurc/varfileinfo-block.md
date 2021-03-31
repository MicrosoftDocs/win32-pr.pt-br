---
title: Instrução VarFileInfo BLOCK
description: Descreve a forma do bloco de informações da variável.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menus de instrução VarFileInfo BLOCK e outros recursos
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006692"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="6d97e-104">Instrução VarFileInfo BLOCK</span><span class="sxs-lookup"><span data-stu-id="6d97e-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="6d97e-105">Define um bloco de informações de variável.</span><span class="sxs-lookup"><span data-stu-id="6d97e-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="6d97e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d97e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d97e-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="6d97e-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="6d97e-108">Um dos identificadores de idioma especificados na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="6d97e-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6d97e-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="6d97e-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="6d97e-110">Um dos identificadores de conjunto de caracteres especificados na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="6d97e-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d97e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d97e-111">Remarks</span></span>

<span data-ttu-id="6d97e-112">Mais de um par de identificadores pode ser fornecido, mas cada par deve ser separado do par anterior com uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="6d97e-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="6d97e-113">O parâmetro *LangID* especifica um dos seguintes códigos de idioma.</span><span class="sxs-lookup"><span data-stu-id="6d97e-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="6d97e-114">Código</span><span class="sxs-lookup"><span data-stu-id="6d97e-114">Code</span></span>   | <span data-ttu-id="6d97e-115">Idioma</span><span class="sxs-lookup"><span data-stu-id="6d97e-115">Language</span></span>            | <span data-ttu-id="6d97e-116">Código</span><span class="sxs-lookup"><span data-stu-id="6d97e-116">Code</span></span>   | <span data-ttu-id="6d97e-117">Idioma</span><span class="sxs-lookup"><span data-stu-id="6d97e-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="6d97e-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="6d97e-118">0x0401</span></span> | <span data-ttu-id="6d97e-119">Árabe</span><span class="sxs-lookup"><span data-stu-id="6d97e-119">Arabic</span></span>              | <span data-ttu-id="6d97e-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="6d97e-120">0x0415</span></span> | <span data-ttu-id="6d97e-121">Polonês</span><span class="sxs-lookup"><span data-stu-id="6d97e-121">Polish</span></span>                    |
| <span data-ttu-id="6d97e-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="6d97e-122">0x0402</span></span> | <span data-ttu-id="6d97e-123">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="6d97e-123">Bulgarian</span></span>           | <span data-ttu-id="6d97e-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="6d97e-124">0x0416</span></span> | <span data-ttu-id="6d97e-125">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="6d97e-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="6d97e-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="6d97e-126">0x0403</span></span> | <span data-ttu-id="6d97e-127">Catalão</span><span class="sxs-lookup"><span data-stu-id="6d97e-127">Catalan</span></span>             | <span data-ttu-id="6d97e-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="6d97e-128">0x0417</span></span> | <span data-ttu-id="6d97e-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="6d97e-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="6d97e-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="6d97e-130">0x0404</span></span> | <span data-ttu-id="6d97e-131">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="6d97e-131">Traditional Chinese</span></span> | <span data-ttu-id="6d97e-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="6d97e-132">0x0418</span></span> | <span data-ttu-id="6d97e-133">Romeno</span><span class="sxs-lookup"><span data-stu-id="6d97e-133">Romanian</span></span>                  |
| <span data-ttu-id="6d97e-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="6d97e-134">0x0405</span></span> | <span data-ttu-id="6d97e-135">Tcheco</span><span class="sxs-lookup"><span data-stu-id="6d97e-135">Czech</span></span>               | <span data-ttu-id="6d97e-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="6d97e-136">0x0419</span></span> | <span data-ttu-id="6d97e-137">Russo</span><span class="sxs-lookup"><span data-stu-id="6d97e-137">Russian</span></span>                   |
| <span data-ttu-id="6d97e-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="6d97e-138">0x0406</span></span> | <span data-ttu-id="6d97e-139">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="6d97e-139">Danish</span></span>              | <span data-ttu-id="6d97e-140">0x041A</span><span class="sxs-lookup"><span data-stu-id="6d97e-140">0x041A</span></span> | <span data-ttu-id="6d97e-141">Croato-Serbian (latino)</span><span class="sxs-lookup"><span data-stu-id="6d97e-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="6d97e-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="6d97e-142">0x0407</span></span> | <span data-ttu-id="6d97e-143">Alemão</span><span class="sxs-lookup"><span data-stu-id="6d97e-143">German</span></span>              | <span data-ttu-id="6d97e-144">0x041B</span><span class="sxs-lookup"><span data-stu-id="6d97e-144">0x041B</span></span> | <span data-ttu-id="6d97e-145">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="6d97e-145">Slovak</span></span>                    |
| <span data-ttu-id="6d97e-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="6d97e-146">0x0408</span></span> | <span data-ttu-id="6d97e-147">Grego</span><span class="sxs-lookup"><span data-stu-id="6d97e-147">Greek</span></span>               | <span data-ttu-id="6d97e-148">0x041C</span><span class="sxs-lookup"><span data-stu-id="6d97e-148">0x041C</span></span> | <span data-ttu-id="6d97e-149">Albanês</span><span class="sxs-lookup"><span data-stu-id="6d97e-149">Albanian</span></span>                  |
| <span data-ttu-id="6d97e-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="6d97e-150">0x0409</span></span> | <span data-ttu-id="6d97e-151">Inglês americano</span><span class="sxs-lookup"><span data-stu-id="6d97e-151">U.S. English</span></span>        | <span data-ttu-id="6d97e-152">0x041D</span><span class="sxs-lookup"><span data-stu-id="6d97e-152">0x041D</span></span> | <span data-ttu-id="6d97e-153">Sueco</span><span class="sxs-lookup"><span data-stu-id="6d97e-153">Swedish</span></span>                   |
| <span data-ttu-id="6d97e-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="6d97e-154">0x040A</span></span> | <span data-ttu-id="6d97e-155">Castelhano espanhol</span><span class="sxs-lookup"><span data-stu-id="6d97e-155">Castilian Spanish</span></span>   | <span data-ttu-id="6d97e-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="6d97e-156">0x041E</span></span> | <span data-ttu-id="6d97e-157">Tailandês</span><span class="sxs-lookup"><span data-stu-id="6d97e-157">Thai</span></span>                      |
| <span data-ttu-id="6d97e-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="6d97e-158">0x040B</span></span> | <span data-ttu-id="6d97e-159">Finlandês</span><span class="sxs-lookup"><span data-stu-id="6d97e-159">Finnish</span></span>             | <span data-ttu-id="6d97e-160">0x041F</span><span class="sxs-lookup"><span data-stu-id="6d97e-160">0x041F</span></span> | <span data-ttu-id="6d97e-161">Turco</span><span class="sxs-lookup"><span data-stu-id="6d97e-161">Turkish</span></span>                   |
| <span data-ttu-id="6d97e-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="6d97e-162">0x040C</span></span> | <span data-ttu-id="6d97e-163">Francês</span><span class="sxs-lookup"><span data-stu-id="6d97e-163">French</span></span>              | <span data-ttu-id="6d97e-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="6d97e-164">0x0420</span></span> | <span data-ttu-id="6d97e-165">Urdu</span><span class="sxs-lookup"><span data-stu-id="6d97e-165">Urdu</span></span>                      |
| <span data-ttu-id="6d97e-166">0x040D</span><span class="sxs-lookup"><span data-stu-id="6d97e-166">0x040D</span></span> | <span data-ttu-id="6d97e-167">Hebraico</span><span class="sxs-lookup"><span data-stu-id="6d97e-167">Hebrew</span></span>              | <span data-ttu-id="6d97e-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="6d97e-168">0x0421</span></span> | <span data-ttu-id="6d97e-169">Bahasa</span><span class="sxs-lookup"><span data-stu-id="6d97e-169">Bahasa</span></span>                    |
| <span data-ttu-id="6d97e-170">0x040E</span><span class="sxs-lookup"><span data-stu-id="6d97e-170">0x040E</span></span> | <span data-ttu-id="6d97e-171">Húngaro</span><span class="sxs-lookup"><span data-stu-id="6d97e-171">Hungarian</span></span>           | <span data-ttu-id="6d97e-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="6d97e-172">0x0804</span></span> | <span data-ttu-id="6d97e-173">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="6d97e-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="6d97e-174">0x040F</span><span class="sxs-lookup"><span data-stu-id="6d97e-174">0x040F</span></span> | <span data-ttu-id="6d97e-175">Islandês</span><span class="sxs-lookup"><span data-stu-id="6d97e-175">Icelandic</span></span>           | <span data-ttu-id="6d97e-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="6d97e-176">0x0807</span></span> | <span data-ttu-id="6d97e-177">Alemão suíço</span><span class="sxs-lookup"><span data-stu-id="6d97e-177">Swiss German</span></span>              |
| <span data-ttu-id="6d97e-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="6d97e-178">0x0410</span></span> | <span data-ttu-id="6d97e-179">Italiano</span><span class="sxs-lookup"><span data-stu-id="6d97e-179">Italian</span></span>             | <span data-ttu-id="6d97e-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="6d97e-180">0x0809</span></span> | <span data-ttu-id="6d97e-181">Inglaterra</span><span class="sxs-lookup"><span data-stu-id="6d97e-181">U.K.</span></span> <span data-ttu-id="6d97e-182">Inglês</span><span class="sxs-lookup"><span data-stu-id="6d97e-182">English</span></span>              |
| <span data-ttu-id="6d97e-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="6d97e-183">0x0411</span></span> | <span data-ttu-id="6d97e-184">Japonês</span><span class="sxs-lookup"><span data-stu-id="6d97e-184">Japanese</span></span>            | <span data-ttu-id="6d97e-185">0x080A</span><span class="sxs-lookup"><span data-stu-id="6d97e-185">0x080A</span></span> | <span data-ttu-id="6d97e-186">Espanhol (México)</span><span class="sxs-lookup"><span data-stu-id="6d97e-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="6d97e-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="6d97e-187">0x0412</span></span> | <span data-ttu-id="6d97e-188">Coreano</span><span class="sxs-lookup"><span data-stu-id="6d97e-188">Korean</span></span>              | <span data-ttu-id="6d97e-189">0x080C</span><span class="sxs-lookup"><span data-stu-id="6d97e-189">0x080C</span></span> | <span data-ttu-id="6d97e-190">Francês belga</span><span class="sxs-lookup"><span data-stu-id="6d97e-190">Belgian French</span></span>            |
| <span data-ttu-id="6d97e-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="6d97e-191">0x0413</span></span> | <span data-ttu-id="6d97e-192">Holandês</span><span class="sxs-lookup"><span data-stu-id="6d97e-192">Dutch</span></span>               | <span data-ttu-id="6d97e-193">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="6d97e-193">0x0C0C</span></span> | <span data-ttu-id="6d97e-194">Francês do Canadá</span><span class="sxs-lookup"><span data-stu-id="6d97e-194">Canadian French</span></span>           |
| <span data-ttu-id="6d97e-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="6d97e-195">0x0414</span></span> | <span data-ttu-id="6d97e-196">Norueguês – Bokmal</span><span class="sxs-lookup"><span data-stu-id="6d97e-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="6d97e-197">0x100C</span><span class="sxs-lookup"><span data-stu-id="6d97e-197">0x100C</span></span> | <span data-ttu-id="6d97e-198">Francês suíço</span><span class="sxs-lookup"><span data-stu-id="6d97e-198">Swiss French</span></span>              |
| <span data-ttu-id="6d97e-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="6d97e-199">0x0810</span></span> | <span data-ttu-id="6d97e-200">Italiano suíço</span><span class="sxs-lookup"><span data-stu-id="6d97e-200">Swiss Italian</span></span>       | <span data-ttu-id="6d97e-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="6d97e-201">0x0816</span></span> | <span data-ttu-id="6d97e-202">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="6d97e-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="6d97e-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="6d97e-203">0x0813</span></span> | <span data-ttu-id="6d97e-204">Holandês belga</span><span class="sxs-lookup"><span data-stu-id="6d97e-204">Belgian Dutch</span></span>       | <span data-ttu-id="6d97e-205">0x081A</span><span class="sxs-lookup"><span data-stu-id="6d97e-205">0x081A</span></span> | <span data-ttu-id="6d97e-206">Serbo-Croatian (cirílico)</span><span class="sxs-lookup"><span data-stu-id="6d97e-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="6d97e-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="6d97e-207">0x0814</span></span> | <span data-ttu-id="6d97e-208">Norueguês – Nynorsk</span><span class="sxs-lookup"><span data-stu-id="6d97e-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="6d97e-209">?</span><span class="sxs-lookup"><span data-stu-id="6d97e-209">?</span></span>      | <span data-ttu-id="6d97e-210">?</span><span class="sxs-lookup"><span data-stu-id="6d97e-210">?</span></span>                         |



 

<span data-ttu-id="6d97e-211">O parâmetro *charsetID* especifica um dos seguintes identificadores de conjunto de caracteres:</span><span class="sxs-lookup"><span data-stu-id="6d97e-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="6d97e-212">Identificador</span><span class="sxs-lookup"><span data-stu-id="6d97e-212">Identifier</span></span> | <span data-ttu-id="6d97e-213">Conjunto de caracteres</span><span class="sxs-lookup"><span data-stu-id="6d97e-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="6d97e-214">0</span><span class="sxs-lookup"><span data-stu-id="6d97e-214">0</span></span>          | <span data-ttu-id="6d97e-215">ASCII de 7 bits</span><span class="sxs-lookup"><span data-stu-id="6d97e-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="6d97e-216">932</span><span class="sxs-lookup"><span data-stu-id="6d97e-216">932</span></span>        | <span data-ttu-id="6d97e-217">Japão (Shift – JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="6d97e-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="6d97e-218">949</span><span class="sxs-lookup"><span data-stu-id="6d97e-218">949</span></span>        | <span data-ttu-id="6d97e-219">Coreia (Shift – KS 5601)</span><span class="sxs-lookup"><span data-stu-id="6d97e-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="6d97e-220">950</span><span class="sxs-lookup"><span data-stu-id="6d97e-220">950</span></span>        | <span data-ttu-id="6d97e-221">Taiwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="6d97e-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="6d97e-222">1200</span><span class="sxs-lookup"><span data-stu-id="6d97e-222">1200</span></span>       | <span data-ttu-id="6d97e-223">Unicode</span><span class="sxs-lookup"><span data-stu-id="6d97e-223">Unicode</span></span>                    |
| <span data-ttu-id="6d97e-224">1250</span><span class="sxs-lookup"><span data-stu-id="6d97e-224">1250</span></span>       | <span data-ttu-id="6d97e-225">Latim-2 (Europa Oriental)</span><span class="sxs-lookup"><span data-stu-id="6d97e-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="6d97e-226">1251</span><span class="sxs-lookup"><span data-stu-id="6d97e-226">1251</span></span>       | <span data-ttu-id="6d97e-227">Cirílico</span><span class="sxs-lookup"><span data-stu-id="6d97e-227">Cyrillic</span></span>                   |
| <span data-ttu-id="6d97e-228">1252</span><span class="sxs-lookup"><span data-stu-id="6d97e-228">1252</span></span>       | <span data-ttu-id="6d97e-229">Multilíngüe</span><span class="sxs-lookup"><span data-stu-id="6d97e-229">Multilingual</span></span>               |
| <span data-ttu-id="6d97e-230">1253</span><span class="sxs-lookup"><span data-stu-id="6d97e-230">1253</span></span>       | <span data-ttu-id="6d97e-231">Grego</span><span class="sxs-lookup"><span data-stu-id="6d97e-231">Greek</span></span>                      |
| <span data-ttu-id="6d97e-232">1254</span><span class="sxs-lookup"><span data-stu-id="6d97e-232">1254</span></span>       | <span data-ttu-id="6d97e-233">Turco</span><span class="sxs-lookup"><span data-stu-id="6d97e-233">Turkish</span></span>                    |
| <span data-ttu-id="6d97e-234">1255</span><span class="sxs-lookup"><span data-stu-id="6d97e-234">1255</span></span>       | <span data-ttu-id="6d97e-235">Hebraico</span><span class="sxs-lookup"><span data-stu-id="6d97e-235">Hebrew</span></span>                     |
| <span data-ttu-id="6d97e-236">1256</span><span class="sxs-lookup"><span data-stu-id="6d97e-236">1256</span></span>       | <span data-ttu-id="6d97e-237">Árabe</span><span class="sxs-lookup"><span data-stu-id="6d97e-237">Arabic</span></span>                     |



 

 

 




