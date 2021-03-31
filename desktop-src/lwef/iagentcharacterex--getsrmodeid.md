---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640224"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="666c5-103">IAgentCharacterEx::GetSRModeID</span><span class="sxs-lookup"><span data-stu-id="666c5-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="666c5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="666c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="666c5-105">Recupera a ID de modo do mecanismo de reconhecimento de fala definido para o caractere.</span><span class="sxs-lookup"><span data-stu-id="666c5-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="666c5-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="666c5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="666c5-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="666c5-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="666c5-108">Endereço de um BSTR que recebe a configuração de ID de modo do mecanismo de reconhecimento de fala para o caractere.</span><span class="sxs-lookup"><span data-stu-id="666c5-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="666c5-109">Essa configuração retorna o mecanismo definido para a entrada de fala de um caractere.</span><span class="sxs-lookup"><span data-stu-id="666c5-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="666c5-110">A ID de modo para um mecanismo de reconhecimento de fala é uma representação de cadeia de caracteres do GUID (formatado com chaves e traços) pelo fornecedor de fala identificando exclusivamente o mecanismo.</span><span class="sxs-lookup"><span data-stu-id="666c5-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="666c5-111">Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="666c5-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="666c5-112">Se você não definir uma ID de modo de mecanismo de reconhecimento de fala para o caractere, o servidor retornará um mecanismo que corresponda à configuração de idioma do caractere (usando as interfaces do Microsoft Speech API).</span><span class="sxs-lookup"><span data-stu-id="666c5-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="666c5-113">Se não houver nenhum mecanismo de reconhecimento de fala correspondente disponível para o caractere, o servidor retornará uma cadeia de caracteres nula (vazia).</span><span class="sxs-lookup"><span data-stu-id="666c5-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="666c5-114">Quando a entrada de fala está habilitada (na janela Opções de caractere avançado), a consulta ou a configuração dessa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="666c5-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="666c5-115">Ou seja, a chave de escuta está disponível e a dica de escuta é exibível.</span><span class="sxs-lookup"><span data-stu-id="666c5-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="666c5-116">(A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala e retornará uma cadeia de caracteres nula (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="666c5-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="666c5-117">Essa função retorna apenas a configuração para o uso do caractere do aplicativo cliente; a configuração não reflete outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="666c5-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="666c5-118">Essa função não falhará se [**IAgentSpeechInputProperties:: Getabilited**](iagentspeechinputproperties--getenabled.md) retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="666c5-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="666c5-119">Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="666c5-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="666c5-120">Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.</span><span class="sxs-lookup"><span data-stu-id="666c5-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="666c5-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="666c5-121">See Also</span></span>

[<span data-ttu-id="666c5-122">**IAgentCharacterEx::SetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="666c5-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




