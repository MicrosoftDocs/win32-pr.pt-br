---
title: Propriedade LanguageID
description: Propriedade LanguageID
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292688"
---
# <a name="languageid-property"></a><span data-ttu-id="871d6-103">Propriedade LanguageID</span><span class="sxs-lookup"><span data-stu-id="871d6-103">LanguageID Property</span></span>

<span data-ttu-id="871d6-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="871d6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="871d6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="871d6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="871d6-106">Retorna ou define a ID de idioma do caractere.</span><span class="sxs-lookup"><span data-stu-id="871d6-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="871d6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="871d6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="871d6-108">*Agent. \* \* \* caracteres* \*  **("***Characterid***"). Idioma da linguagemid** \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="871d6-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="871d6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="871d6-109">Part</span></span>

<span data-ttu-id="871d6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="871d6-110">Description</span></span>

<span data-ttu-id="871d6-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="871d6-111">LanguageID</span></span>

<span data-ttu-id="871d6-112">Um inteiro longo que especifica a ID de idioma para o caractere.</span><span class="sxs-lookup"><span data-stu-id="871d6-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="871d6-113">A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="871d6-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="871d6-114">Os exemplos a seguir são valores para idiomas com suporte pelo Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="871d6-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="871d6-115">Para determinar o valor de outros idiomas, consulte a *documentação do Platform SDK*.</span><span class="sxs-lookup"><span data-stu-id="871d6-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="871d6-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="871d6-116">Arabic</span></span>

<span data-ttu-id="871d6-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="871d6-117">&H0401</span></span>

<span data-ttu-id="871d6-118">Italiano</span><span class="sxs-lookup"><span data-stu-id="871d6-118">Italian</span></span>

<span data-ttu-id="871d6-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="871d6-119">&H0410</span></span>

 

<span data-ttu-id="871d6-120">Basco</span><span class="sxs-lookup"><span data-stu-id="871d6-120">Basque</span></span>

<span data-ttu-id="871d6-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="871d6-121">&H042D</span></span>

<span data-ttu-id="871d6-122">Japonês</span><span class="sxs-lookup"><span data-stu-id="871d6-122">Japanese</span></span>

<span data-ttu-id="871d6-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="871d6-123">&H0411</span></span>

 

<span data-ttu-id="871d6-124">Chinês (Simplificado)</span><span class="sxs-lookup"><span data-stu-id="871d6-124">Chinese (Simplified)</span></span>

<span data-ttu-id="871d6-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="871d6-125">&H0804</span></span>

<span data-ttu-id="871d6-126">Coreano</span><span class="sxs-lookup"><span data-stu-id="871d6-126">Korean</span></span>

<span data-ttu-id="871d6-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="871d6-127">&H0412</span></span>

 

<span data-ttu-id="871d6-128">Chinês (Tradicional)</span><span class="sxs-lookup"><span data-stu-id="871d6-128">Chinese (Traditional)</span></span>

<span data-ttu-id="871d6-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="871d6-129">&H0404</span></span>

<span data-ttu-id="871d6-130">Norueguês</span><span class="sxs-lookup"><span data-stu-id="871d6-130">Norwegian</span></span>

<span data-ttu-id="871d6-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="871d6-131">&H0414</span></span>

 

<span data-ttu-id="871d6-132">Croata</span><span class="sxs-lookup"><span data-stu-id="871d6-132">Croatian</span></span>

<span data-ttu-id="871d6-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="871d6-133">&H041A</span></span>

<span data-ttu-id="871d6-134">Polonês</span><span class="sxs-lookup"><span data-stu-id="871d6-134">Polish</span></span>

<span data-ttu-id="871d6-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="871d6-135">&H0415</span></span>

 

<span data-ttu-id="871d6-136">Tcheco</span><span class="sxs-lookup"><span data-stu-id="871d6-136">Czech</span></span>

<span data-ttu-id="871d6-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="871d6-137">&H0405</span></span>

<span data-ttu-id="871d6-138">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="871d6-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="871d6-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="871d6-139">&H0816</span></span>

 

<span data-ttu-id="871d6-140">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="871d6-140">Danish</span></span>

<span data-ttu-id="871d6-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="871d6-141">&H0406</span></span>

<span data-ttu-id="871d6-142">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="871d6-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="871d6-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="871d6-143">&H0416</span></span>

 

<span data-ttu-id="871d6-144">Holandês</span><span class="sxs-lookup"><span data-stu-id="871d6-144">Dutch</span></span>

<span data-ttu-id="871d6-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="871d6-145">&H0413</span></span>

<span data-ttu-id="871d6-146">Romeno</span><span class="sxs-lookup"><span data-stu-id="871d6-146">Romanian</span></span>

<span data-ttu-id="871d6-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="871d6-147">&H0418</span></span>

 

<span data-ttu-id="871d6-148">Inglês (britânico)</span><span class="sxs-lookup"><span data-stu-id="871d6-148">English (British)</span></span>

<span data-ttu-id="871d6-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="871d6-149">&H0809</span></span>

<span data-ttu-id="871d6-150">Russo</span><span class="sxs-lookup"><span data-stu-id="871d6-150">Russian</span></span>

<span data-ttu-id="871d6-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="871d6-151">&H0419</span></span>

 

<span data-ttu-id="871d6-152">Inglês (EUA)</span><span class="sxs-lookup"><span data-stu-id="871d6-152">English (US)</span></span>

<span data-ttu-id="871d6-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="871d6-153">&H0409</span></span>

<span data-ttu-id="871d6-154">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="871d6-154">Slovakian</span></span>

<span data-ttu-id="871d6-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="871d6-155">&H041B</span></span>

 

<span data-ttu-id="871d6-156">Finlandês</span><span class="sxs-lookup"><span data-stu-id="871d6-156">Finnish</span></span>

<span data-ttu-id="871d6-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="871d6-157">&H040B</span></span>

<span data-ttu-id="871d6-158">Esloveno</span><span class="sxs-lookup"><span data-stu-id="871d6-158">Slovenian</span></span>

<span data-ttu-id="871d6-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="871d6-159">&H0424</span></span>

 

<span data-ttu-id="871d6-160">Francês</span><span class="sxs-lookup"><span data-stu-id="871d6-160">French</span></span>

<span data-ttu-id="871d6-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="871d6-161">&H040C</span></span>

<span data-ttu-id="871d6-162">Espanhol</span><span class="sxs-lookup"><span data-stu-id="871d6-162">Spanish</span></span>

<span data-ttu-id="871d6-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="871d6-163">&H0C0A</span></span>

 

<span data-ttu-id="871d6-164">Alemão</span><span class="sxs-lookup"><span data-stu-id="871d6-164">German</span></span>

<span data-ttu-id="871d6-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="871d6-165">&H0407</span></span>

<span data-ttu-id="871d6-166">Sueco</span><span class="sxs-lookup"><span data-stu-id="871d6-166">Swedish</span></span>

<span data-ttu-id="871d6-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="871d6-167">&H041D</span></span>

 

<span data-ttu-id="871d6-168">Grego</span><span class="sxs-lookup"><span data-stu-id="871d6-168">Greek</span></span>

<span data-ttu-id="871d6-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="871d6-169">&H0408</span></span>

<span data-ttu-id="871d6-170">Tailandês</span><span class="sxs-lookup"><span data-stu-id="871d6-170">Thai</span></span>

<span data-ttu-id="871d6-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="871d6-171">&H041E</span></span>

 

<span data-ttu-id="871d6-172">Hebraico</span><span class="sxs-lookup"><span data-stu-id="871d6-172">Hebrew</span></span>

<span data-ttu-id="871d6-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="871d6-173">&H040D</span></span>

<span data-ttu-id="871d6-174">Turco</span><span class="sxs-lookup"><span data-stu-id="871d6-174">Turkish</span></span>

<span data-ttu-id="871d6-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="871d6-175">&H041F</span></span>

 

<span data-ttu-id="871d6-176">Húngaro</span><span class="sxs-lookup"><span data-stu-id="871d6-176">Hungarian</span></span>

<span data-ttu-id="871d6-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="871d6-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="871d6-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="871d6-178">Remarks</span></span>

<span data-ttu-id="871d6-179">Se você não definir **LanguageID** para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL do idioma do agente correspondente estiver instalada, caso contrário, o idioma do caractere será inglês (EUA).</span><span class="sxs-lookup"><span data-stu-id="871d6-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="871d6-180">Essa propriedade também determina o idioma do texto de balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="871d6-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="871d6-181">Ele também determina o idioma padrão para a saída de TTS.</span><span class="sxs-lookup"><span data-stu-id="871d6-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="871d6-182">Se você tentar definir **LanguageID** para um caractere e a DLL de idioma do agente para esse idioma não estiver instalada ou uma fonte de exibição para a ID do idioma não estiver disponível, o Agent gerará um erro e **LanguageID** permanecerá em sua última configuração.</span><span class="sxs-lookup"><span data-stu-id="871d6-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="871d6-183">Definir essa propriedade não gerará um erro se não houver mecanismos de fala correspondentes para o idioma.</span><span class="sxs-lookup"><span data-stu-id="871d6-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="871d6-184">Para determinar se há um mecanismo de fala compatível disponível para o **LanguageID**, verifique [**SRModeID**](srmodeid-property.md) ou [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="871d6-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="871d6-185">Se você não definir **LanguageID**, ele será definido como a configuração de ID de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="871d6-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="871d6-186">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="871d6-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="871d6-187">Se você definir **LanguageID** como uma linguagem que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema executando seu aplicativo não tiver suporte bidirecional instalado, o texto na palavra balão aparecerá em lógica em vez de em ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="871d6-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="871d6-188">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="871d6-188">See Also</span></span>

<span data-ttu-id="871d6-189">[**Propriedade SRModeID**](srmodeid-property.md), [ **Propriedade TTSModeID**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="871d6-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




