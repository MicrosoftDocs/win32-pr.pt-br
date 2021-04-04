---
title: Método de escuta
description: Método de escuta
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007419"
---
# <a name="listen-method"></a><span data-ttu-id="2bcac-103">Método de escuta</span><span class="sxs-lookup"><span data-stu-id="2bcac-103">Listen Method</span></span>

<span data-ttu-id="2bcac-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2bcac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2bcac-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="2bcac-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2bcac-106">Ativa o modo de escuta (reconhecimento de fala) por um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="2bcac-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="2bcac-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="2bcac-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2bcac-108">\*agente do. ***Caracteres \* \* \* \* ("*** characterid \* \* *").* \*  *Estado* de escuta</span><span class="sxs-lookup"><span data-stu-id="2bcac-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="2bcac-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2bcac-109">Part</span></span>    | <span data-ttu-id="2bcac-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bcac-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcac-111">*State*</span><span class="sxs-lookup"><span data-stu-id="2bcac-111">*State*</span></span> | <span data-ttu-id="2bcac-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="2bcac-112">Required.</span></span> <span data-ttu-id="2bcac-113">Um valor booliano que determina se o modo de escuta deve ser ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="2bcac-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="2bcac-114">**Verdadeiro** Ativa o modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="2bcac-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="2bcac-115">**Falso** Desativa o modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="2bcac-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bcac-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bcac-116">Remarks</span></span>

<span data-ttu-id="2bcac-117">Definir esse método como **true** habilita o modo de escuta (ativa o reconhecimento de fala) por um período de tempo fixo (10 segundos).</span><span class="sxs-lookup"><span data-stu-id="2bcac-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="2bcac-118">Embora não seja possível definir o valor do tempo limite, você pode desligar o modo de escuta antes que o tempo limite expire.</span><span class="sxs-lookup"><span data-stu-id="2bcac-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="2bcac-119">Se você (ou outro cliente) tiver definido o modo de escuta com êxito e tentar definir essa propriedade como **true** antes da expiração do tempo limite, o método terá êxito e redefinirá o tempo limite. No entanto, se o modo de escuta estiver ativado porque o usuário está pressionando a tecla de escuta, o método terá sucesso, mas o tempo limite será ignorado e o modo de escuta terminará com base na interação do usuário com a chave de escuta.</span><span class="sxs-lookup"><span data-stu-id="2bcac-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="2bcac-120">Esse método tem sucesso apenas quando chamado pelo cliente de entrada-ativo e se os serviços de fala foram iniciados.</span><span class="sxs-lookup"><span data-stu-id="2bcac-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="2bcac-121">Para garantir que os serviços de fala tenham sido iniciados, consulte ou defina o [**SRModeID**](srmodeid-property.md) ou defina a configuração de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) antes de chamar **Listen** , caso contrário, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="2bcac-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="2bcac-122">Para detectar o sucesso desse método, chame-o como uma função e ele retornará um valor booliano indicando se o método teve êxito.</span><span class="sxs-lookup"><span data-stu-id="2bcac-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="2bcac-123">O método também falhará se o usuário estiver pressionando a tecla de escuta e você tentar definir **escutar** como **false**.</span><span class="sxs-lookup"><span data-stu-id="2bcac-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="2bcac-124">No entanto, se o usuário tiver liberado a chave de escuta e o modo de escuta não tiver expirado, ele terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="2bcac-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="2bcac-125">A **escuta** também falhará se não houver nenhum mecanismo de fala compatível disponível que corresponda à configuração [**LanguageID**](languageid-property.md) do caractere, o usuário desabilitou a entrada de fala usando a folha de propriedades do Microsoft Agent ou o dispositivo de áudio está ocupado.</span><span class="sxs-lookup"><span data-stu-id="2bcac-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="2bcac-126">Quando você define com êxito esse método como **true**, o servidor dispara o evento [**ListenStart**](listenstart-event.md) .</span><span class="sxs-lookup"><span data-stu-id="2bcac-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="2bcac-127">O servidor envia [**ListenComplete**](listencomplete-event.md) quando o tempo limite do modo de escuta é concluído ou quando você define **Listen** como **false**.</span><span class="sxs-lookup"><span data-stu-id="2bcac-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="2bcac-128">Esse método não chama automaticamente [**Stop**](stop-method.md) e executa uma animação de estado de escuta conforme o servidor faz quando a tecla de escuta é pressionada.</span><span class="sxs-lookup"><span data-stu-id="2bcac-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="2bcac-129">Isso permite que você determine se deve interromper a animação atual usando a animação [**ListenStart**](listenstart-event.md) chamando **Stop** e jogando sua própria animação apropriada.</span><span class="sxs-lookup"><span data-stu-id="2bcac-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="2bcac-130">No entanto, o servidor chama **Stop** e executa uma animação de estado audição quando um usuário expressão é detectado.</span><span class="sxs-lookup"><span data-stu-id="2bcac-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bcac-131">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2bcac-131">See Also</span></span>

<span data-ttu-id="2bcac-132">[**Propriedade LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="2bcac-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

