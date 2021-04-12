---
title: GetStatus do IAgentAudioOutputPropertiesEx
description: GetStatus do IAgentAudioOutputPropertiesEx
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364163"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="dbf34-103">IAgentAudioOutputPropertiesEx:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="dbf34-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="dbf34-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dbf34-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="dbf34-105">Recupera o status do canal de áudio.</span><span class="sxs-lookup"><span data-stu-id="dbf34-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="dbf34-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dbf34-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dbf34-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="dbf34-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="dbf34-108">Status do canal de saída de áudio, que pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="dbf34-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="dbf34-109">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf34-109">Value</span></span>                                                                         | <span data-ttu-id="dbf34-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbf34-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf34-111">const status de áudio **curto sem sinal** **\_ \_ disponível = 0;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="dbf34-112">O canal de saída de áudio está disponível (não ocupado).</span><span class="sxs-lookup"><span data-stu-id="dbf34-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="dbf34-113">const status de áudio **curto não assinado** **\_ \_ noáudio = 1;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="dbf34-114">Não há suporte para saída de áudio; por exemplo, como não há placa de som.</span><span class="sxs-lookup"><span data-stu-id="dbf34-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="dbf34-115">const status de áudio **curto não assinado** **\_ \_ CANTOPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="dbf34-116">O canal de saída de áudio não pode ser aberto (está ocupado); por exemplo, como outro aplicativo está reproduzindo áudio.</span><span class="sxs-lookup"><span data-stu-id="dbf34-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="dbf34-117">const status de áudio **curto sem sinal** **\_ \_ userfalando = 3;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="dbf34-118">O canal de saída de áudio está ocupado porque o servidor está processando a entrada de fala do usuário</span><span class="sxs-lookup"><span data-stu-id="dbf34-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="dbf34-119">const status de áudio **curto não assinado** **\_ \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="dbf34-120">O canal de saída de áudio está ocupado porque um caractere está falando no momento.</span><span class="sxs-lookup"><span data-stu-id="dbf34-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="dbf34-121">const status de áudio **curto não assinado** **\_ \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="dbf34-122">O canal de saída de áudio não está ocupado, mas está aguardando a entrada de fala do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbf34-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="dbf34-123">const erro de status de áudio **curto não assinado** **\_ \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="dbf34-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="dbf34-124">Houve algum outro problema (desconhecido) ao tentar acessar o canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="dbf34-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="dbf34-125">Essa configuração permite que o aplicativo cliente consulte o estado do canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="dbf34-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="dbf34-126">Você pode usar isso para determinar se seu caractere deve falar ou tentar ativar o modo de escuta (usando [**IAgentCharacterEx:: Listen**](lwef.iagentcharacterex::listen_method)).</span><span class="sxs-lookup"><span data-stu-id="dbf34-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using [**IAgentCharacterEx::Listen**](lwef.iagentcharacterex::listen_method)).</span></span>

 

 





