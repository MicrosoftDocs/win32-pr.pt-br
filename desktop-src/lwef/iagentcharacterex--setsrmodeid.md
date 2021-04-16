---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104453850"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="53616-103">IAgentCharacterEx::SetSRModeID</span><span class="sxs-lookup"><span data-stu-id="53616-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="53616-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53616-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="53616-105">Define a ID de modo do mecanismo de reconhecimento de fala definido para o caractere.</span><span class="sxs-lookup"><span data-stu-id="53616-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="53616-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="53616-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="53616-107">bszModeID</span><span class="sxs-lookup"><span data-stu-id="53616-107">bszModeID</span></span>

<span data-ttu-id="53616-108">A configuração de ID de modo do mecanismo de reconhecimento de fala para o caractere.</span><span class="sxs-lookup"><span data-stu-id="53616-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="53616-109">Essa configuração define o mecanismo para a entrada de fala de um caractere.</span><span class="sxs-lookup"><span data-stu-id="53616-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="53616-110">A ID de modo para um mecanismo de reconhecimento de fala é o GUID definido pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo (formatado com chaves e traços).</span><span class="sxs-lookup"><span data-stu-id="53616-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="53616-111">Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="53616-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="53616-112">Se você especificar uma ID de modo que não corresponda à configuração de idioma do caractere, se o usuário tiver desabilitado o reconhecimento de fala (na folha de propriedades do Microsoft Agent) ou se o mecanismo não estiver instalado, essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="53616-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="53616-113">Se você não definir uma ID de modo de mecanismo de reconhecimento de fala para o caractere, o servidor definirá uma que corresponda à configuração de idioma do caractere (usando as interfaces do Microsoft Speech API).</span><span class="sxs-lookup"><span data-stu-id="53616-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="53616-114">Quando a entrada de fala está habilitada na folha de propriedades do agente (opções avançadas de caractere), a definição dessa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="53616-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="53616-115">Ou seja, a chave de escuta está disponível e a dica de escuta é exibível.</span><span class="sxs-lookup"><span data-stu-id="53616-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="53616-116">(A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="53616-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="53616-117">Essa propriedade aplica-se somente ao cliente do caractere; a configuração não reflete a configuração para outros clientes do caractere ou outros caracteres do cliente.</span><span class="sxs-lookup"><span data-stu-id="53616-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="53616-118">Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="53616-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="53616-119">Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.</span><span class="sxs-lookup"><span data-stu-id="53616-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="53616-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="53616-120">See Also</span></span>

[<span data-ttu-id="53616-121">**IAgentCharacterEx::GetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="53616-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




