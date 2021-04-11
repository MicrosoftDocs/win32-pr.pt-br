---
title: Escuta IAgentCharacterEx
description: Escuta IAgentCharacterEx
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292363"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="02f82-103">IAgentCharacterEx:: escutar</span><span class="sxs-lookup"><span data-stu-id="02f82-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="02f82-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02f82-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="02f82-105">Ativa ou desativa o modo de escuta (entrada de reconhecimento de fala).</span><span class="sxs-lookup"><span data-stu-id="02f82-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="02f82-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="02f82-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="02f82-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span><span class="sxs-lookup"><span data-stu-id="02f82-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="02f82-108">Sinalizador de modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="02f82-108">Listening mode flag.</span></span> <span data-ttu-id="02f82-109">Se esse parâmetro for **true**, o modo de escuta será ativado; Se for **false**, o modo de escuta será desativado.</span><span class="sxs-lookup"><span data-stu-id="02f82-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="02f82-110">Definir esse método como **true** habilita o modo de escuta (ativa o reconhecimento de fala) por um período de tempo fixo.</span><span class="sxs-lookup"><span data-stu-id="02f82-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="02f82-111">Embora não seja possível definir o valor do tempo limite, você pode desligar o modo de escuta antes que o tempo limite expire.</span><span class="sxs-lookup"><span data-stu-id="02f82-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="02f82-112">Além disso, se o modo de escuta já estiver ativo porque você (ou outro cliente) definiu com êxito o método como **verdadeiro** antes de expirar o tempo limite, o método terá êxito e redefinirá o tempo limite. No entanto, se o modo de escuta já estiver ativado porque o usuário está pressionando a tecla de escuta, o método terá sucesso, mas o tempo limite será ignorado e o modo de escuta terminará com base na interação do usuário com a chave de escuta.</span><span class="sxs-lookup"><span data-stu-id="02f82-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="02f82-113">Esse método terá sucesso somente quando chamado pelo cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="02f82-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="02f82-114">Portanto, o método falhará se o cliente não for o cliente ativo do caractere superior.</span><span class="sxs-lookup"><span data-stu-id="02f82-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="02f82-115">O método também falhará se você tentar definir o método como **false** e o usuário estiver pressionando a tecla de escuta.</span><span class="sxs-lookup"><span data-stu-id="02f82-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="02f82-116">Ele também pode falhar se não houver nenhum mecanismo de fala compatível disponível que corresponda à configuração de ID de idioma do caractere ou o usuário tenha desabilitado a entrada de fala usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="02f82-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="02f82-117">No entanto, o método não falhará se o dispositivo de áudio estiver ocupado.</span><span class="sxs-lookup"><span data-stu-id="02f82-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="02f82-118">Quando você define com êxito esse método como **true**, o servidor dispara o evento [**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md) .</span><span class="sxs-lookup"><span data-stu-id="02f82-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="02f82-119">O servidor também envia **IAgentNotifySinkEx:: listeningstate** quando o tempo limite do modo de escuta é concluído ou quando você define [**IAgentCharacterEx:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) como **false**.</span><span class="sxs-lookup"><span data-stu-id="02f82-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="02f82-120">Esse método não chama automaticamente [**IAgentCharacter:: Enopall**](iagentcharacter--stopall.md) e executa uma animação de estado de escuta do caractere, como ocorre quando o usuário pressiona a tecla de escuta.</span><span class="sxs-lookup"><span data-stu-id="02f82-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="02f82-121">Isso permite que você use o evento [**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md) para determinar se deseja parar a animação atual e executar sua própria animação apropriada.</span><span class="sxs-lookup"><span data-stu-id="02f82-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="02f82-122">No entanto, quando um usuário expressão é detectado, o servidor chama automaticamente **IAgentCharacter:: Adopall** e desempenha uma animação de estado audição.</span><span class="sxs-lookup"><span data-stu-id="02f82-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="02f82-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="02f82-123">See Also</span></span>

<span data-ttu-id="02f82-124">[**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties:: getabilited**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="02f82-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




