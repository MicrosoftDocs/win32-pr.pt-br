---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365671"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="7cb80-103">IAgentCharacterEx::SetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="7cb80-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="7cb80-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7cb80-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="7cb80-105">Define a ID de modo do mecanismo de TTS definido para o caractere.</span><span class="sxs-lookup"><span data-stu-id="7cb80-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="7cb80-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7cb80-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7cb80-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span><span class="sxs-lookup"><span data-stu-id="7cb80-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="7cb80-108">A configuração de ID de modo do mecanismo de TTS para o caractere.</span><span class="sxs-lookup"><span data-stu-id="7cb80-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="7cb80-109">**IAgentCharacterEx: SetTTSModeID** pode falhar se o Speech.dll não estiver instalado e o mecanismo especificado não corresponder à configuração do modo TTS compilado do caractere.</span><span class="sxs-lookup"><span data-stu-id="7cb80-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="7cb80-110">Essa configuração determina o modo de mecanismo preferencial para a saída de TTS falada de um caractere.</span><span class="sxs-lookup"><span data-stu-id="7cb80-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="7cb80-111">A ID de modo para um mecanismo de TTS (conversão de texto em fala) é o GUID definido pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo (formatado com chaves e traços).</span><span class="sxs-lookup"><span data-stu-id="7cb80-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="7cb80-112">Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="7cb80-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="7cb80-113">Se você definir uma ID de modo TTS, ela substituirá a tentativa do servidor de corresponder a um mecanismo de fala com base na ID do modo TTS compilado do caractere, na ID do idioma atual do sistema e na ID de idioma atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="7cb80-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="7cb80-114">No entanto, se você tentar definir uma ID de modo quando o usuário tiver desabilitado a saída de fala na folha de propriedades do Microsoft Agent ou quando o mecanismo associado não estiver instalado, essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="7cb80-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="7cb80-115">Se você não definir uma ID de modo de mecanismo TTS para o caractere, o servidor definirá um mecanismo que corresponda à configuração de idioma do caractere (usando as interfaces do Microsoft Speech API).</span><span class="sxs-lookup"><span data-stu-id="7cb80-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="7cb80-116">A definição dessa propriedade carregará o mecanismo associado se ele ainda não estiver carregado.</span><span class="sxs-lookup"><span data-stu-id="7cb80-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="7cb80-117">Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="7cb80-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="7cb80-118">Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="7cb80-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="7cb80-119">Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.</span><span class="sxs-lookup"><span data-stu-id="7cb80-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cb80-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7cb80-120">See Also</span></span>

[<span data-ttu-id="7cb80-121">**IAgentCharacterEx:GetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="7cb80-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




