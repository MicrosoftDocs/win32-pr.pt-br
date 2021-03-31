---
title: IAgentCharacterEx setlanguageid
description: IAgentCharacterEx setlanguageid
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635361"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="b9f69-103">IAgentCharacterEx:: setlanguageid</span><span class="sxs-lookup"><span data-stu-id="b9f69-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="b9f69-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b9f69-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="b9f69-105">Define o ID de idioma definido para o caractere.</span><span class="sxs-lookup"><span data-stu-id="b9f69-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="b9f69-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b9f69-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b9f69-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="b9f69-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="b9f69-108">A configuração de ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="b9f69-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="b9f69-109">Um inteiro longo que especifica a ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="b9f69-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="b9f69-110">A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="b9f69-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="b9f69-111">Você pode usar os seguintes valores para os idiomas especificados.</span><span class="sxs-lookup"><span data-stu-id="b9f69-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="b9f69-112">Para obter mais informações, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="b9f69-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="b9f69-113">Árabe (Arábia)</span><span class="sxs-lookup"><span data-stu-id="b9f69-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="b9f69-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="b9f69-114">0x0401</span></span> | <span data-ttu-id="b9f69-115">Italiano</span><span class="sxs-lookup"><span data-stu-id="b9f69-115">Italian</span></span>               | <span data-ttu-id="b9f69-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="b9f69-116">0x0410</span></span> |
| <span data-ttu-id="b9f69-117">Basco</span><span class="sxs-lookup"><span data-stu-id="b9f69-117">Basque</span></span>                | <span data-ttu-id="b9f69-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="b9f69-118">0x042d</span></span> | <span data-ttu-id="b9f69-119">Japonês</span><span class="sxs-lookup"><span data-stu-id="b9f69-119">Japanese</span></span>              | <span data-ttu-id="b9f69-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="b9f69-120">0x0411</span></span> |
| <span data-ttu-id="b9f69-121">Chinês (Simplificado)</span><span class="sxs-lookup"><span data-stu-id="b9f69-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="b9f69-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="b9f69-122">0x0804</span></span> | <span data-ttu-id="b9f69-123">Coreano</span><span class="sxs-lookup"><span data-stu-id="b9f69-123">Korean</span></span>                | <span data-ttu-id="b9f69-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="b9f69-124">0x0412</span></span> |
| <span data-ttu-id="b9f69-125">Chinês (Tradicional)</span><span class="sxs-lookup"><span data-stu-id="b9f69-125">Chinese (Traditional)</span></span> | <span data-ttu-id="b9f69-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="b9f69-126">0x0404</span></span> | <span data-ttu-id="b9f69-127">Norueguês</span><span class="sxs-lookup"><span data-stu-id="b9f69-127">Norwegian</span></span>             | <span data-ttu-id="b9f69-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="b9f69-128">0x0414</span></span> |
| <span data-ttu-id="b9f69-129">Croata</span><span class="sxs-lookup"><span data-stu-id="b9f69-129">Croatian</span></span>              | <span data-ttu-id="b9f69-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="b9f69-130">0x041A</span></span> | <span data-ttu-id="b9f69-131">Polonês</span><span class="sxs-lookup"><span data-stu-id="b9f69-131">Polish</span></span>                | <span data-ttu-id="b9f69-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="b9f69-132">0x0415</span></span> |
| <span data-ttu-id="b9f69-133">Tcheco</span><span class="sxs-lookup"><span data-stu-id="b9f69-133">Czech</span></span>                 | <span data-ttu-id="b9f69-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="b9f69-134">0x0405</span></span> | <span data-ttu-id="b9f69-135">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="b9f69-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="b9f69-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="b9f69-136">0x0816</span></span> |
| <span data-ttu-id="b9f69-137">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="b9f69-137">Danish</span></span>                | <span data-ttu-id="b9f69-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="b9f69-138">0x0406</span></span> | <span data-ttu-id="b9f69-139">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="b9f69-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="b9f69-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="b9f69-140">0x0416</span></span> |
| <span data-ttu-id="b9f69-141">Holandês</span><span class="sxs-lookup"><span data-stu-id="b9f69-141">Dutch</span></span>                 | <span data-ttu-id="b9f69-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="b9f69-142">0x0413</span></span> | <span data-ttu-id="b9f69-143">Romeno</span><span class="sxs-lookup"><span data-stu-id="b9f69-143">Romanian</span></span>              | <span data-ttu-id="b9f69-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="b9f69-144">0x0418</span></span> |
| <span data-ttu-id="b9f69-145">Inglês (britânico)</span><span class="sxs-lookup"><span data-stu-id="b9f69-145">English (British)</span></span>     | <span data-ttu-id="b9f69-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="b9f69-146">0x0809</span></span> | <span data-ttu-id="b9f69-147">Russo</span><span class="sxs-lookup"><span data-stu-id="b9f69-147">Russian</span></span>               | <span data-ttu-id="b9f69-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="b9f69-148">0x0419</span></span> |
| <span data-ttu-id="b9f69-149">Inglês (EUA)</span><span class="sxs-lookup"><span data-stu-id="b9f69-149">English (US)</span></span>          | <span data-ttu-id="b9f69-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="b9f69-150">0x0409</span></span> | <span data-ttu-id="b9f69-151">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="b9f69-151">Slovakian</span></span>             | <span data-ttu-id="b9f69-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="b9f69-152">0x041B</span></span> |
| <span data-ttu-id="b9f69-153">Finlandês</span><span class="sxs-lookup"><span data-stu-id="b9f69-153">Finnish</span></span>               | <span data-ttu-id="b9f69-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="b9f69-154">0x040B</span></span> | <span data-ttu-id="b9f69-155">Esloveno</span><span class="sxs-lookup"><span data-stu-id="b9f69-155">Slovenian</span></span>             | <span data-ttu-id="b9f69-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="b9f69-156">0x0424</span></span> |
| <span data-ttu-id="b9f69-157">Francês</span><span class="sxs-lookup"><span data-stu-id="b9f69-157">French</span></span>                | <span data-ttu-id="b9f69-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="b9f69-158">0x040C</span></span> | <span data-ttu-id="b9f69-159">Espanhol</span><span class="sxs-lookup"><span data-stu-id="b9f69-159">Spanish</span></span>               | <span data-ttu-id="b9f69-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="b9f69-160">0x0C0A</span></span> |
| <span data-ttu-id="b9f69-161">Alemão</span><span class="sxs-lookup"><span data-stu-id="b9f69-161">German</span></span>                | <span data-ttu-id="b9f69-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="b9f69-162">0x0407</span></span> | <span data-ttu-id="b9f69-163">Sueco</span><span class="sxs-lookup"><span data-stu-id="b9f69-163">Swedish</span></span>               | <span data-ttu-id="b9f69-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="b9f69-164">0x041D</span></span> |
| <span data-ttu-id="b9f69-165">Grego</span><span class="sxs-lookup"><span data-stu-id="b9f69-165">Greek</span></span>                 | <span data-ttu-id="b9f69-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="b9f69-166">0x0408</span></span> | <span data-ttu-id="b9f69-167">Tailandês</span><span class="sxs-lookup"><span data-stu-id="b9f69-167">Thai</span></span>                  | <span data-ttu-id="b9f69-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="b9f69-168">0x041E</span></span> |
| <span data-ttu-id="b9f69-169">Hebraico</span><span class="sxs-lookup"><span data-stu-id="b9f69-169">Hebrew</span></span>                | <span data-ttu-id="b9f69-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="b9f69-170">0x040D</span></span> | <span data-ttu-id="b9f69-171">Turco</span><span class="sxs-lookup"><span data-stu-id="b9f69-171">Turkish</span></span>               | <span data-ttu-id="b9f69-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="b9f69-172">0x041F</span></span> |
| <span data-ttu-id="b9f69-173">Húngaro</span><span class="sxs-lookup"><span data-stu-id="b9f69-173">Hungarian</span></span>             | <span data-ttu-id="b9f69-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="b9f69-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="b9f69-175">Se você não definir a ID de idioma para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL do idioma do agente correspondente estiver instalada; caso contrário, o idioma do caractere será inglês (EUA).</span><span class="sxs-lookup"><span data-stu-id="b9f69-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="b9f69-176">Essa propriedade também determina o idioma do texto do balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="b9f69-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="b9f69-177">Ele também determina o idioma padrão para a saída de TTS.</span><span class="sxs-lookup"><span data-stu-id="b9f69-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="b9f69-178">Para determinar se há um mecanismo de fala compatível disponível para o idioma do caractere, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="b9f69-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="b9f69-179">Se você tentar definir a ID de idioma para um caractere e os recursos de idioma do agente, a página de código ou uma fonte de exibição para a ID do idioma não estiver disponível, o Agent retornará um erro e a ID do idioma do caractere permanecerá em sua última configuração.</span><span class="sxs-lookup"><span data-stu-id="b9f69-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="b9f69-180">Definir essa propriedade não retornará um erro se não houver nenhum mecanismo de fala correspondente para o idioma.</span><span class="sxs-lookup"><span data-stu-id="b9f69-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="b9f69-181">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="b9f69-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="b9f69-182">Se você definir a ID de idioma do caractere como um idioma que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema que executa o aplicativo não tem suporte bidirecional instalado, o texto aparecerá no balão de palavras em lógica em vez de em ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="b9f69-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b9f69-183">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b9f69-183">See Also</span></span>

<span data-ttu-id="b9f69-184">[**IAgentCharacterEx: Getlanguageid**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="b9f69-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




