---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007189"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="ad8c0-103">IAgentCharacterEx::GetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="ad8c0-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="ad8c0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ad8c0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="ad8c0-105">Recupera a ID de modo do mecanismo TTS definido para o caractere.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="ad8c0-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ad8c0-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="ad8c0-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="ad8c0-108">Endereço de um BSTR que recebe a configuração de ID de modo do mecanismo de TTS para o caractere.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="ad8c0-109">Essa configuração retorna a ID do modo de mecanismo de TTS (conversão de texto em fala) para a saída falada de um caractere.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="ad8c0-110">A ID de modo para um mecanismo de TTS é uma representação de cadeia de caracteres do GUID (formatado com chaves e traços) definido pelo fornecedor de fala identificando exclusivamente o mecanismo.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="ad8c0-111">Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad8c0-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="ad8c0-112">A consulta dessa propriedade carregará o mecanismo associado se ele ainda não estiver carregado.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="ad8c0-113">Se você não definir uma ID de modo de mecanismo TTS para o caractere, o servidor tentará retornar um mecanismo que corresponda (usando as interfaces do Microsoft Speech API) a configuração de TTS compilada do caractere e a configuração de idioma atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="ad8c0-114">Se forem diferentes, a configuração de idioma do caractere substituirá sua configuração de modo criado.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="ad8c0-115">Se você não tiver definido a configuração de idioma do caractere, o idioma do caractere será a ID de idioma padrão do usuário e o servidor tentará a correspondência com base na ID do idioma.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="ad8c0-116">Essa função não falhará se [**IAgentAudioObjectProperties:: Getabilited**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="ad8c0-117">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="ad8c0-118">Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="ad8c0-119">Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.</span><span class="sxs-lookup"><span data-stu-id="ad8c0-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad8c0-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ad8c0-120">See Also</span></span>

[<span data-ttu-id="ad8c0-121">**IAgentCharacterEx::SetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="ad8c0-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




