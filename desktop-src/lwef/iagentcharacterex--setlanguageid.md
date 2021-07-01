---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119001"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="4278b-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="4278b-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="4278b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4278b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="4278b-105">Define a ID de idioma definida para o caractere.</span><span class="sxs-lookup"><span data-stu-id="4278b-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="4278b-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4278b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4278b-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*</span><span class="sxs-lookup"><span data-stu-id="4278b-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="4278b-108">A configuração de ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="4278b-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="4278b-109">Um inteiro Longo que especifica a ID de idioma do caractere.</span><span class="sxs-lookup"><span data-stu-id="4278b-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="4278b-110">A LANGID (ID de idioma) de um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="4278b-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="4278b-111">Você pode usar os valores a seguir para os idiomas especificados.</span><span class="sxs-lookup"><span data-stu-id="4278b-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="4278b-112">Para obter mais informações, consulte a documentação do SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="4278b-112">For more information, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="4278b-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="4278b-113">Language</span></span>              | <span data-ttu-id="4278b-114">ID</span><span class="sxs-lookup"><span data-stu-id="4278b-114">ID</span></span>     |  <span data-ttu-id="4278b-115">Idioma</span><span class="sxs-lookup"><span data-stu-id="4278b-115">Language</span></span>             | <span data-ttu-id="4278b-116">ID</span><span class="sxs-lookup"><span data-stu-id="4278b-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="4278b-117">Árabe (Árabe)</span><span class="sxs-lookup"><span data-stu-id="4278b-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="4278b-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="4278b-118">0x0401</span></span> | <span data-ttu-id="4278b-119">Italiano</span><span class="sxs-lookup"><span data-stu-id="4278b-119">Italian</span></span>               | <span data-ttu-id="4278b-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="4278b-120">0x0410</span></span> |
| <span data-ttu-id="4278b-121">Basco</span><span class="sxs-lookup"><span data-stu-id="4278b-121">Basque</span></span>                | <span data-ttu-id="4278b-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="4278b-122">0x042d</span></span> | <span data-ttu-id="4278b-123">Japonês</span><span class="sxs-lookup"><span data-stu-id="4278b-123">Japanese</span></span>              | <span data-ttu-id="4278b-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="4278b-124">0x0411</span></span> |
| <span data-ttu-id="4278b-125">Chinês (Simplificado)</span><span class="sxs-lookup"><span data-stu-id="4278b-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="4278b-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="4278b-126">0x0804</span></span> | <span data-ttu-id="4278b-127">Coreano</span><span class="sxs-lookup"><span data-stu-id="4278b-127">Korean</span></span>                | <span data-ttu-id="4278b-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="4278b-128">0x0412</span></span> |
| <span data-ttu-id="4278b-129">Chinês (Tradicional)</span><span class="sxs-lookup"><span data-stu-id="4278b-129">Chinese (Traditional)</span></span> | <span data-ttu-id="4278b-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="4278b-130">0x0404</span></span> | <span data-ttu-id="4278b-131">Norueguês</span><span class="sxs-lookup"><span data-stu-id="4278b-131">Norwegian</span></span>             | <span data-ttu-id="4278b-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="4278b-132">0x0414</span></span> |
| <span data-ttu-id="4278b-133">Croata</span><span class="sxs-lookup"><span data-stu-id="4278b-133">Croatian</span></span>              | <span data-ttu-id="4278b-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="4278b-134">0x041A</span></span> | <span data-ttu-id="4278b-135">Polonês</span><span class="sxs-lookup"><span data-stu-id="4278b-135">Polish</span></span>                | <span data-ttu-id="4278b-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="4278b-136">0x0415</span></span> |
| <span data-ttu-id="4278b-137">Tcheco</span><span class="sxs-lookup"><span data-stu-id="4278b-137">Czech</span></span>                 | <span data-ttu-id="4278b-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="4278b-138">0x0405</span></span> | <span data-ttu-id="4278b-139">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="4278b-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="4278b-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="4278b-140">0x0816</span></span> |
| <span data-ttu-id="4278b-141">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="4278b-141">Danish</span></span>                | <span data-ttu-id="4278b-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="4278b-142">0x0406</span></span> | <span data-ttu-id="4278b-143">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="4278b-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="4278b-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="4278b-144">0x0416</span></span> |
| <span data-ttu-id="4278b-145">Holandês</span><span class="sxs-lookup"><span data-stu-id="4278b-145">Dutch</span></span>                 | <span data-ttu-id="4278b-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="4278b-146">0x0413</span></span> | <span data-ttu-id="4278b-147">Romeno</span><span class="sxs-lookup"><span data-stu-id="4278b-147">Romanian</span></span>              | <span data-ttu-id="4278b-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="4278b-148">0x0418</span></span> |
| <span data-ttu-id="4278b-149">Inglês (britânico)</span><span class="sxs-lookup"><span data-stu-id="4278b-149">English (British)</span></span>     | <span data-ttu-id="4278b-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="4278b-150">0x0809</span></span> | <span data-ttu-id="4278b-151">Russo</span><span class="sxs-lookup"><span data-stu-id="4278b-151">Russian</span></span>               | <span data-ttu-id="4278b-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="4278b-152">0x0419</span></span> |
| <span data-ttu-id="4278b-153">Inglês (EUA)</span><span class="sxs-lookup"><span data-stu-id="4278b-153">English (US)</span></span>          | <span data-ttu-id="4278b-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="4278b-154">0x0409</span></span> | <span data-ttu-id="4278b-155">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="4278b-155">Slovakian</span></span>             | <span data-ttu-id="4278b-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="4278b-156">0x041B</span></span> |
| <span data-ttu-id="4278b-157">Finlandês</span><span class="sxs-lookup"><span data-stu-id="4278b-157">Finnish</span></span>               | <span data-ttu-id="4278b-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="4278b-158">0x040B</span></span> | <span data-ttu-id="4278b-159">Esloveno</span><span class="sxs-lookup"><span data-stu-id="4278b-159">Slovenian</span></span>             | <span data-ttu-id="4278b-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="4278b-160">0x0424</span></span> |
| <span data-ttu-id="4278b-161">Francês</span><span class="sxs-lookup"><span data-stu-id="4278b-161">French</span></span>                | <span data-ttu-id="4278b-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="4278b-162">0x040C</span></span> | <span data-ttu-id="4278b-163">Espanhol</span><span class="sxs-lookup"><span data-stu-id="4278b-163">Spanish</span></span>               | <span data-ttu-id="4278b-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="4278b-164">0x0C0A</span></span> |
| <span data-ttu-id="4278b-165">Alemão</span><span class="sxs-lookup"><span data-stu-id="4278b-165">German</span></span>                | <span data-ttu-id="4278b-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="4278b-166">0x0407</span></span> | <span data-ttu-id="4278b-167">Sueco</span><span class="sxs-lookup"><span data-stu-id="4278b-167">Swedish</span></span>               | <span data-ttu-id="4278b-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="4278b-168">0x041D</span></span> |
| <span data-ttu-id="4278b-169">Grego</span><span class="sxs-lookup"><span data-stu-id="4278b-169">Greek</span></span>                 | <span data-ttu-id="4278b-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="4278b-170">0x0408</span></span> | <span data-ttu-id="4278b-171">Tailandês</span><span class="sxs-lookup"><span data-stu-id="4278b-171">Thai</span></span>                  | <span data-ttu-id="4278b-172">0x041e</span><span class="sxs-lookup"><span data-stu-id="4278b-172">0x041E</span></span> |
| <span data-ttu-id="4278b-173">Hebraico</span><span class="sxs-lookup"><span data-stu-id="4278b-173">Hebrew</span></span>                | <span data-ttu-id="4278b-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="4278b-174">0x040D</span></span> | <span data-ttu-id="4278b-175">Turco</span><span class="sxs-lookup"><span data-stu-id="4278b-175">Turkish</span></span>               | <span data-ttu-id="4278b-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="4278b-176">0x041F</span></span> |
| <span data-ttu-id="4278b-177">Húngaro</span><span class="sxs-lookup"><span data-stu-id="4278b-177">Hungarian</span></span>             | <span data-ttu-id="4278b-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="4278b-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="4278b-179">Se você não definir a ID de idioma para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL de idioma do Agent correspondente estiver instalada; caso contrário, o idioma do caractere será Inglês (EUA).</span><span class="sxs-lookup"><span data-stu-id="4278b-179">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="4278b-180">Essa propriedade também determina o idioma da palavra texto de balão, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="4278b-180">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="4278b-181">Ele também determina o idioma padrão para a saída do TTS.</span><span class="sxs-lookup"><span data-stu-id="4278b-181">It also determines the default language for TTS output.</span></span> <span data-ttu-id="4278b-182">Para determinar se há um mecanismo de fala compatível disponível para a linguagem do caractere, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="4278b-182">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="4278b-183">Se você tentar definir a ID de idioma para um caractere e os recursos de linguagem do Agent, a página de código ou uma fonte de exibição para a ID do idioma não estiver disponível, o Agent retornará um erro e a ID do idioma do caractere permanecerá em sua última configuração.</span><span class="sxs-lookup"><span data-stu-id="4278b-183">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="4278b-184">Definir essa propriedade não retornará um erro se não houver mecanismos de fala correspondentes para o idioma.</span><span class="sxs-lookup"><span data-stu-id="4278b-184">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="4278b-185">Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4278b-185">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="4278b-186">Se você definir a ID de idioma do caractere para um idioma que dá suporte a texto bidirecional (como árabe ou hebraico), mas o sistema que executa seu aplicativo não tiver suporte bidirecional instalado, o texto aparecerá na palavra balão em ordem lógica em vez de exibir.</span><span class="sxs-lookup"><span data-stu-id="4278b-186">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4278b-187">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4278b-187">See Also</span></span>

<span data-ttu-id="4278b-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="4278b-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




