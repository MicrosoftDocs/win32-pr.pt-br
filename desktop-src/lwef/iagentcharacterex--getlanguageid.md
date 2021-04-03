---
title: IAgentCharacterEx getlanguageid
description: IAgentCharacterEx getlanguageid
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005875"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="0071c-103">IAgentCharacterEx:: getlanguageid</span><span class="sxs-lookup"><span data-stu-id="0071c-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="0071c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0071c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="0071c-105">Recupera o conjunto de ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="0071c-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="0071c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0071c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0071c-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="0071c-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="0071c-108">Endereço de uma variável que recebe a configuração de ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="0071c-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="0071c-109">Um inteiro longo que especifica a ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="0071c-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="0071c-110">A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="0071c-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="0071c-111">Os exemplos a seguir são valores para alguns idiomas.</span><span class="sxs-lookup"><span data-stu-id="0071c-111">The following examples are values for some languages.</span></span> <span data-ttu-id="0071c-112">Para determinar os valores de outros idiomas, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0071c-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="0071c-113">Árabe (Arábia)</span><span class="sxs-lookup"><span data-stu-id="0071c-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="0071c-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="0071c-114">0x0401</span></span> | <span data-ttu-id="0071c-115">Italiano</span><span class="sxs-lookup"><span data-stu-id="0071c-115">Italian</span></span>               | <span data-ttu-id="0071c-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="0071c-116">0x0410</span></span> |
| <span data-ttu-id="0071c-117">Basco</span><span class="sxs-lookup"><span data-stu-id="0071c-117">Basque</span></span>                | <span data-ttu-id="0071c-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="0071c-118">0x042d</span></span> | <span data-ttu-id="0071c-119">Japonês</span><span class="sxs-lookup"><span data-stu-id="0071c-119">Japanese</span></span>              | <span data-ttu-id="0071c-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="0071c-120">0x0411</span></span> |
| <span data-ttu-id="0071c-121">Chinês (Simplificado)</span><span class="sxs-lookup"><span data-stu-id="0071c-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="0071c-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="0071c-122">0x0804</span></span> | <span data-ttu-id="0071c-123">Coreano</span><span class="sxs-lookup"><span data-stu-id="0071c-123">Korean</span></span>                | <span data-ttu-id="0071c-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="0071c-124">0x0412</span></span> |
| <span data-ttu-id="0071c-125">Chinês (Tradicional)</span><span class="sxs-lookup"><span data-stu-id="0071c-125">Chinese (Traditional)</span></span> | <span data-ttu-id="0071c-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="0071c-126">0x0404</span></span> | <span data-ttu-id="0071c-127">Norueguês</span><span class="sxs-lookup"><span data-stu-id="0071c-127">Norwegian</span></span>             | <span data-ttu-id="0071c-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="0071c-128">0x0414</span></span> |
| <span data-ttu-id="0071c-129">Croata</span><span class="sxs-lookup"><span data-stu-id="0071c-129">Croatian</span></span>              | <span data-ttu-id="0071c-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="0071c-130">0x041A</span></span> | <span data-ttu-id="0071c-131">Polonês</span><span class="sxs-lookup"><span data-stu-id="0071c-131">Polish</span></span>                | <span data-ttu-id="0071c-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="0071c-132">0x0415</span></span> |
| <span data-ttu-id="0071c-133">Tcheco</span><span class="sxs-lookup"><span data-stu-id="0071c-133">Czech</span></span>                 | <span data-ttu-id="0071c-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="0071c-134">0x0405</span></span> | <span data-ttu-id="0071c-135">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="0071c-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="0071c-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="0071c-136">0x0816</span></span> |
| <span data-ttu-id="0071c-137">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="0071c-137">Danish</span></span>                | <span data-ttu-id="0071c-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="0071c-138">0x0406</span></span> | <span data-ttu-id="0071c-139">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="0071c-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="0071c-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="0071c-140">0x0416</span></span> |
| <span data-ttu-id="0071c-141">Holandês</span><span class="sxs-lookup"><span data-stu-id="0071c-141">Dutch</span></span>                 | <span data-ttu-id="0071c-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="0071c-142">0x0413</span></span> | <span data-ttu-id="0071c-143">Romeno</span><span class="sxs-lookup"><span data-stu-id="0071c-143">Romanian</span></span>              | <span data-ttu-id="0071c-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="0071c-144">0x0418</span></span> |
| <span data-ttu-id="0071c-145">Inglês (britânico)</span><span class="sxs-lookup"><span data-stu-id="0071c-145">English (British)</span></span>     | <span data-ttu-id="0071c-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="0071c-146">0x0809</span></span> | <span data-ttu-id="0071c-147">Russo</span><span class="sxs-lookup"><span data-stu-id="0071c-147">Russian</span></span>               | <span data-ttu-id="0071c-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="0071c-148">0x0419</span></span> |
| <span data-ttu-id="0071c-149">Inglês (EUA)</span><span class="sxs-lookup"><span data-stu-id="0071c-149">English (US)</span></span>          | <span data-ttu-id="0071c-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="0071c-150">0x0409</span></span> | <span data-ttu-id="0071c-151">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="0071c-151">Slovakian</span></span>             | <span data-ttu-id="0071c-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="0071c-152">0x041B</span></span> |
| <span data-ttu-id="0071c-153">Finlandês</span><span class="sxs-lookup"><span data-stu-id="0071c-153">Finnish</span></span>               | <span data-ttu-id="0071c-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="0071c-154">0x040B</span></span> | <span data-ttu-id="0071c-155">Esloveno</span><span class="sxs-lookup"><span data-stu-id="0071c-155">Slovenian</span></span>             | <span data-ttu-id="0071c-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="0071c-156">0x0424</span></span> |
| <span data-ttu-id="0071c-157">Francês</span><span class="sxs-lookup"><span data-stu-id="0071c-157">French</span></span>                | <span data-ttu-id="0071c-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="0071c-158">0x040C</span></span> | <span data-ttu-id="0071c-159">Espanhol</span><span class="sxs-lookup"><span data-stu-id="0071c-159">Spanish</span></span>               | <span data-ttu-id="0071c-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="0071c-160">0x0C0A</span></span> |
| <span data-ttu-id="0071c-161">Alemão</span><span class="sxs-lookup"><span data-stu-id="0071c-161">German</span></span>                | <span data-ttu-id="0071c-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="0071c-162">0x0407</span></span> | <span data-ttu-id="0071c-163">Sueco</span><span class="sxs-lookup"><span data-stu-id="0071c-163">Swedish</span></span>               | <span data-ttu-id="0071c-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="0071c-164">0x041D</span></span> |
| <span data-ttu-id="0071c-165">Grego</span><span class="sxs-lookup"><span data-stu-id="0071c-165">Greek</span></span>                 | <span data-ttu-id="0071c-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="0071c-166">0x0408</span></span> | <span data-ttu-id="0071c-167">Tailandês</span><span class="sxs-lookup"><span data-stu-id="0071c-167">Thai</span></span>                  | <span data-ttu-id="0071c-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="0071c-168">0x041E</span></span> |
| <span data-ttu-id="0071c-169">Hebraico</span><span class="sxs-lookup"><span data-stu-id="0071c-169">Hebrew</span></span>                | <span data-ttu-id="0071c-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="0071c-170">0x040D</span></span> | <span data-ttu-id="0071c-171">Turco</span><span class="sxs-lookup"><span data-stu-id="0071c-171">Turkish</span></span>               | <span data-ttu-id="0071c-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="0071c-172">0x041F</span></span> |
| <span data-ttu-id="0071c-173">Húngaro</span><span class="sxs-lookup"><span data-stu-id="0071c-173">Hungarian</span></span>             | <span data-ttu-id="0071c-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="0071c-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="0071c-175">Se você não definir essa ID de idioma para o caractere, a ID de idioma do caractere será a ID do idioma atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="0071c-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="0071c-176">Essa configuração também determina o idioma da saída TTS, o texto do balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="0071c-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="0071c-177">Para determinar se há um mecanismo de reconhecimento de fala compatível disponível para o idioma do caractere, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="0071c-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="0071c-178">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0071c-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="0071c-179">Se a ID do idioma for definida como um idioma que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema que executa o aplicativo não tiver suporte bidirecional instalado, o texto aparecerá no balão do Word em ordem lógica, em vez de exibição.</span><span class="sxs-lookup"><span data-stu-id="0071c-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0071c-180">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0071c-180">See Also</span></span>

<span data-ttu-id="0071c-181">[**IAgentCharacterEx: Setlanguageid**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="0071c-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




