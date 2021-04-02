---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005332"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="defb6-103">IAgentCharacterEx::GetSRStatus</span><span class="sxs-lookup"><span data-stu-id="defb6-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="defb6-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="defb6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="defb6-105">Recupera o status da condição necessária para dar suporte à entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="defb6-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="defb6-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="defb6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="defb6-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="defb6-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="defb6-108">Endereço de uma variável que recebe um dos seguintes valores para a configuração de Estado:</span><span class="sxs-lookup"><span data-stu-id="defb6-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="defb6-109">Valor</span><span class="sxs-lookup"><span data-stu-id="defb6-109">Value</span></span>                                                                               | <span data-ttu-id="defb6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="defb6-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="defb6-111">**const não assinada** **status de escuta longa \_ \_ canlistie = 0;**</span><span class="sxs-lookup"><span data-stu-id="defb6-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="defb6-112">As condições dão suporte à entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="defb6-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="defb6-113">const status de escuta **longa sem sinal** **\_ \_ noáudio = 1;**</span><span class="sxs-lookup"><span data-stu-id="defb6-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="defb6-114">Não há nenhum dispositivo de entrada de áudio disponível neste sistema.</span><span class="sxs-lookup"><span data-stu-id="defb6-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="defb6-115">(Observe que isso não detecta se um microfone está instalado; ele só pode detectar se o usuário tem uma placa de som habilitada para entrada devidamente instalada com um driver funcional.)</span><span class="sxs-lookup"><span data-stu-id="defb6-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="defb6-116">const status de escuta **longa não assinado não** **\_ \_ superior = 2;**</span><span class="sxs-lookup"><span data-stu-id="defb6-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="defb6-117">Outro cliente é o cliente ativo desse caractere ou o caractere atual não é o mais alto.</span><span class="sxs-lookup"><span data-stu-id="defb6-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="defb6-118">const status de escuta **longa não assinado** **\_ \_ CANTOPENAUDIO = 3;**</span><span class="sxs-lookup"><span data-stu-id="defb6-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="defb6-119">O canal de entrada ou saída de áudio está ocupado no momento, outro aplicativo está usando áudio.</span><span class="sxs-lookup"><span data-stu-id="defb6-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="defb6-120">const status de escuta **longa não assinado** **\_ \_ COULDNTINITIALIZESPEECH = 4;**</span><span class="sxs-lookup"><span data-stu-id="defb6-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="defb6-121">Ocorreu um erro não especificado no processo de inicialização do subsistema de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="defb6-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="defb6-122">Isso inclui a possibilidade de que não haja um mecanismo de fala disponível correspondente à configuração de idioma do caractere.</span><span class="sxs-lookup"><span data-stu-id="defb6-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="defb6-123">const status de escuta **longa não assinado** **\_ \_ SPEECHDISABLED = 5;**</span><span class="sxs-lookup"><span data-stu-id="defb6-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="defb6-124">O usuário desabilitou a entrada de fala na janela Opções de caractere avançadas.</span><span class="sxs-lookup"><span data-stu-id="defb6-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="defb6-125">const erro de status de escuta **longa sem sinal** **\_ \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="defb6-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="defb6-126">Ocorreu um erro ao verificar o status de áudio, mas a causa do erro não foi retornada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="defb6-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="defb6-127">Essa função permite consultar se as condições atuais dão suporte à entrada de reconhecimento de fala, incluindo o status do dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="defb6-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="defb6-128">Se seu aplicativo usar o método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) , você poderá usar essa função para garantir melhor que a chamada terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="defb6-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="defb6-129">Chamar esse método também carregará o mecanismo de fala se ele ainda não estiver carregado.</span><span class="sxs-lookup"><span data-stu-id="defb6-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="defb6-130">No entanto, ele não ativa o modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="defb6-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="defb6-131">Quando a entrada de fala está habilitada na folha de propriedades do agente (opções avançadas de caractere), a consulta do status carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="defb6-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="defb6-132">Ou seja, a chave de escuta está disponível e a dica de escuta é exibível.</span><span class="sxs-lookup"><span data-stu-id="defb6-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="defb6-133">(A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="defb6-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="defb6-134">Essa função retorna apenas a configuração para o uso do caractere do aplicativo cliente; a configuração não reflete outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="defb6-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





