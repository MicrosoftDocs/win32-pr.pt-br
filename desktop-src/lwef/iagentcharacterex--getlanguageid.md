---
title: IAgentCharacterEx getlanguageid
description: IAgentCharacterEx getlanguageid
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120642"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="235b0-103">IAgentCharacterEx:: getlanguageid</span><span class="sxs-lookup"><span data-stu-id="235b0-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="235b0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="235b0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="235b0-105">Recupera o conjunto de ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="235b0-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="235b0-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="235b0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="235b0-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="235b0-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="235b0-108">Endereço de uma variável que recebe a configuração de ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="235b0-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="235b0-109">Um inteiro longo que especifica a ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="235b0-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="235b0-110">A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="235b0-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="235b0-111">Os exemplos a seguir são valores para alguns idiomas.</span><span class="sxs-lookup"><span data-stu-id="235b0-111">The following examples are values for some languages.</span></span> <span data-ttu-id="235b0-112">Para determinar os valores de outros idiomas, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="235b0-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="235b0-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="235b0-113">Language</span></span>              | <span data-ttu-id="235b0-114">ID</span><span class="sxs-lookup"><span data-stu-id="235b0-114">ID</span></span>     | <span data-ttu-id="235b0-115">Idioma</span><span class="sxs-lookup"><span data-stu-id="235b0-115">Language</span></span>              | <span data-ttu-id="235b0-116">ID</span><span class="sxs-lookup"><span data-stu-id="235b0-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="235b0-117">Árabe (Arábia)</span><span class="sxs-lookup"><span data-stu-id="235b0-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="235b0-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="235b0-118">0x0401</span></span> | <span data-ttu-id="235b0-119">Italiano</span><span class="sxs-lookup"><span data-stu-id="235b0-119">Italian</span></span>               | <span data-ttu-id="235b0-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="235b0-120">0x0410</span></span> |
| <span data-ttu-id="235b0-121">Basco</span><span class="sxs-lookup"><span data-stu-id="235b0-121">Basque</span></span>                | <span data-ttu-id="235b0-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="235b0-122">0x042d</span></span> | <span data-ttu-id="235b0-123">Japonês</span><span class="sxs-lookup"><span data-stu-id="235b0-123">Japanese</span></span>              | <span data-ttu-id="235b0-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="235b0-124">0x0411</span></span> |
| <span data-ttu-id="235b0-125">Chinês (Simplificado)</span><span class="sxs-lookup"><span data-stu-id="235b0-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="235b0-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="235b0-126">0x0804</span></span> | <span data-ttu-id="235b0-127">Coreano</span><span class="sxs-lookup"><span data-stu-id="235b0-127">Korean</span></span>                | <span data-ttu-id="235b0-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="235b0-128">0x0412</span></span> |
| <span data-ttu-id="235b0-129">Chinês (Tradicional)</span><span class="sxs-lookup"><span data-stu-id="235b0-129">Chinese (Traditional)</span></span> | <span data-ttu-id="235b0-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="235b0-130">0x0404</span></span> | <span data-ttu-id="235b0-131">Norueguês</span><span class="sxs-lookup"><span data-stu-id="235b0-131">Norwegian</span></span>             | <span data-ttu-id="235b0-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="235b0-132">0x0414</span></span> |
| <span data-ttu-id="235b0-133">Croata</span><span class="sxs-lookup"><span data-stu-id="235b0-133">Croatian</span></span>              | <span data-ttu-id="235b0-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="235b0-134">0x041A</span></span> | <span data-ttu-id="235b0-135">Polonês</span><span class="sxs-lookup"><span data-stu-id="235b0-135">Polish</span></span>                | <span data-ttu-id="235b0-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="235b0-136">0x0415</span></span> |
| <span data-ttu-id="235b0-137">Tcheco</span><span class="sxs-lookup"><span data-stu-id="235b0-137">Czech</span></span>                 | <span data-ttu-id="235b0-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="235b0-138">0x0405</span></span> | <span data-ttu-id="235b0-139">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="235b0-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="235b0-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="235b0-140">0x0816</span></span> |
| <span data-ttu-id="235b0-141">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="235b0-141">Danish</span></span>                | <span data-ttu-id="235b0-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="235b0-142">0x0406</span></span> | <span data-ttu-id="235b0-143">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="235b0-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="235b0-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="235b0-144">0x0416</span></span> |
| <span data-ttu-id="235b0-145">Holandês</span><span class="sxs-lookup"><span data-stu-id="235b0-145">Dutch</span></span>                 | <span data-ttu-id="235b0-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="235b0-146">0x0413</span></span> | <span data-ttu-id="235b0-147">Romeno</span><span class="sxs-lookup"><span data-stu-id="235b0-147">Romanian</span></span>              | <span data-ttu-id="235b0-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="235b0-148">0x0418</span></span> |
| <span data-ttu-id="235b0-149">Inglês (britânico)</span><span class="sxs-lookup"><span data-stu-id="235b0-149">English (British)</span></span>     | <span data-ttu-id="235b0-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="235b0-150">0x0809</span></span> | <span data-ttu-id="235b0-151">Russo</span><span class="sxs-lookup"><span data-stu-id="235b0-151">Russian</span></span>               | <span data-ttu-id="235b0-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="235b0-152">0x0419</span></span> |
| <span data-ttu-id="235b0-153">Inglês (EUA)</span><span class="sxs-lookup"><span data-stu-id="235b0-153">English (US)</span></span>          | <span data-ttu-id="235b0-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="235b0-154">0x0409</span></span> | <span data-ttu-id="235b0-155">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="235b0-155">Slovakian</span></span>             | <span data-ttu-id="235b0-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="235b0-156">0x041B</span></span> |
| <span data-ttu-id="235b0-157">Finlandês</span><span class="sxs-lookup"><span data-stu-id="235b0-157">Finnish</span></span>               | <span data-ttu-id="235b0-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="235b0-158">0x040B</span></span> | <span data-ttu-id="235b0-159">Esloveno</span><span class="sxs-lookup"><span data-stu-id="235b0-159">Slovenian</span></span>             | <span data-ttu-id="235b0-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="235b0-160">0x0424</span></span> |
| <span data-ttu-id="235b0-161">Francês</span><span class="sxs-lookup"><span data-stu-id="235b0-161">French</span></span>                | <span data-ttu-id="235b0-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="235b0-162">0x040C</span></span> | <span data-ttu-id="235b0-163">Espanhol</span><span class="sxs-lookup"><span data-stu-id="235b0-163">Spanish</span></span>               | <span data-ttu-id="235b0-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="235b0-164">0x0C0A</span></span> |
| <span data-ttu-id="235b0-165">Alemão</span><span class="sxs-lookup"><span data-stu-id="235b0-165">German</span></span>                | <span data-ttu-id="235b0-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="235b0-166">0x0407</span></span> | <span data-ttu-id="235b0-167">Sueco</span><span class="sxs-lookup"><span data-stu-id="235b0-167">Swedish</span></span>               | <span data-ttu-id="235b0-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="235b0-168">0x041D</span></span> |
| <span data-ttu-id="235b0-169">Grego</span><span class="sxs-lookup"><span data-stu-id="235b0-169">Greek</span></span>                 | <span data-ttu-id="235b0-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="235b0-170">0x0408</span></span> | <span data-ttu-id="235b0-171">Tailandês</span><span class="sxs-lookup"><span data-stu-id="235b0-171">Thai</span></span>                  | <span data-ttu-id="235b0-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="235b0-172">0x041E</span></span> |
| <span data-ttu-id="235b0-173">Hebraico</span><span class="sxs-lookup"><span data-stu-id="235b0-173">Hebrew</span></span>                | <span data-ttu-id="235b0-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="235b0-174">0x040D</span></span> | <span data-ttu-id="235b0-175">Turco</span><span class="sxs-lookup"><span data-stu-id="235b0-175">Turkish</span></span>               | <span data-ttu-id="235b0-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="235b0-176">0x041F</span></span> |
| <span data-ttu-id="235b0-177">Húngaro</span><span class="sxs-lookup"><span data-stu-id="235b0-177">Hungarian</span></span>             | <span data-ttu-id="235b0-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="235b0-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="235b0-179">Se você não definir essa ID de idioma para o caractere, a ID de idioma do caractere será a ID do idioma atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="235b0-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="235b0-180">Essa configuração também determina o idioma da saída TTS, o texto do balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="235b0-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="235b0-181">Para determinar se há um mecanismo de reconhecimento de fala compatível disponível para o idioma do caractere, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="235b0-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="235b0-182">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="235b0-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="235b0-183">Se a ID do idioma for definida como um idioma que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema que executa o aplicativo não tiver suporte bidirecional instalado, o texto aparecerá no balão do Word em ordem lógica, em vez de exibição.</span><span class="sxs-lookup"><span data-stu-id="235b0-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="235b0-184">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="235b0-184">See Also</span></span>

<span data-ttu-id="235b0-185">[**IAgentCharacterEx: Setlanguageid**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="235b0-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




