---
title: Propriedade SRStatus
description: Propriedade SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006186"
---
# <a name="srstatus-property"></a><span data-ttu-id="65b72-103">Propriedade SRStatus</span><span class="sxs-lookup"><span data-stu-id="65b72-103">SRStatus Property</span></span>

<span data-ttu-id="65b72-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65b72-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="65b72-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="65b72-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="65b72-106">Retorna se a entrada de fala pode ser iniciada para o caractere.</span><span class="sxs-lookup"><span data-stu-id="65b72-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="65b72-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="65b72-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="65b72-108">*Agente. ***Caracteres ("*** characterid \* \* *"). SRStatus**</span><span class="sxs-lookup"><span data-stu-id="65b72-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="65b72-109">Valor</span><span class="sxs-lookup"><span data-stu-id="65b72-109">Value</span></span> | <span data-ttu-id="65b72-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="65b72-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b72-111">0</span><span class="sxs-lookup"><span data-stu-id="65b72-111">0</span></span>     | <span data-ttu-id="65b72-112">As condições dão suporte à entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="65b72-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="65b72-113">1</span><span class="sxs-lookup"><span data-stu-id="65b72-113">1</span></span>     | <span data-ttu-id="65b72-114">Não há nenhum dispositivo de entrada de áudio disponível neste sistema.</span><span class="sxs-lookup"><span data-stu-id="65b72-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="65b72-115">(Observe que isso não detecta se um microfone está instalado; ele só pode detectar se o usuário tem uma placa de som habilitada para entrada devidamente instalada com um driver funcional.)</span><span class="sxs-lookup"><span data-stu-id="65b72-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="65b72-116">2</span><span class="sxs-lookup"><span data-stu-id="65b72-116">2</span></span>     | <span data-ttu-id="65b72-117">Outro cliente é o cliente ativo desse caractere ou o caractere atual não é o mais alto.</span><span class="sxs-lookup"><span data-stu-id="65b72-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="65b72-118">3</span><span class="sxs-lookup"><span data-stu-id="65b72-118">3</span></span>     | <span data-ttu-id="65b72-119">O canal de entrada ou saída de áudio está ocupado no momento, um aplicativo está usando áudio.</span><span class="sxs-lookup"><span data-stu-id="65b72-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="65b72-120">4</span><span class="sxs-lookup"><span data-stu-id="65b72-120">4</span></span>     | <span data-ttu-id="65b72-121">Ocorreu um erro não especificado no processo de inicialização do subsistema de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="65b72-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="65b72-122">Isso inclui a possibilidade de que não haja um mecanismo de fala disponível correspondente à configuração de idioma do caractere.</span><span class="sxs-lookup"><span data-stu-id="65b72-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="65b72-123">5</span><span class="sxs-lookup"><span data-stu-id="65b72-123">5</span></span>     | <span data-ttu-id="65b72-124">O usuário desabilitou a entrada de fala nas opções de caractere avançado.</span><span class="sxs-lookup"><span data-stu-id="65b72-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="65b72-125">6</span><span class="sxs-lookup"><span data-stu-id="65b72-125">6</span></span>     | <span data-ttu-id="65b72-126">Ocorreu um erro ao verificar o status de áudio, mas a causa do erro não foi retornada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="65b72-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65b72-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="65b72-127">Remarks</span></span>

<span data-ttu-id="65b72-128">Essa propriedade retorna as condições necessárias para dar suporte à entrada de fala, incluindo o status do dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="65b72-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="65b72-129">Você pode verificar essa propriedade antes de chamar o método [**Listen**](listen-method.md) para garantir melhor seu sucesso.</span><span class="sxs-lookup"><span data-stu-id="65b72-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="65b72-130">Quando a entrada de fala está habilitada na folha de propriedades do agente (opções avançadas de caractere), a consulta dessa propriedade carregará o mecanismo associado, se ele ainda não estiver carregado, e iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="65b72-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="65b72-131">Ou seja, a chave de escuta está disponível e a dica de escuta é automaticamente displayável.</span><span class="sxs-lookup"><span data-stu-id="65b72-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="65b72-132">(A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções avançadas de caractere.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="65b72-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="65b72-133">Essa propriedade só se aplica ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="65b72-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="65b72-134">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="65b72-134">See Also</span></span>

[<span data-ttu-id="65b72-135">**Método de escuta**</span><span class="sxs-lookup"><span data-stu-id="65b72-135">**Listen method**</span></span>](listen-method.md)


 

 




