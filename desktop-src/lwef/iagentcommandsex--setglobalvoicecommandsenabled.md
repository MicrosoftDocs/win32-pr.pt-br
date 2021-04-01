---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084504"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="2a244-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="2a244-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="2a244-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a244-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="2a244-105">Define a propriedade [**Enabled**](enabled-property.md) para a gramática de voz dos comandos globais do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2a244-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="2a244-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2a244-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2a244-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span><span class="sxs-lookup"><span data-stu-id="2a244-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="2a244-108">Um valor booliano que define se a gramática de voz dos comandos globais do agente está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2a244-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="2a244-109">**Verdadeiro** habilita a gramática de voz; **False** desabilita.</span><span class="sxs-lookup"><span data-stu-id="2a244-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="2a244-110">O Microsoft Agent adiciona automaticamente parâmetros de voz (gramática) para abrir e fechar a janela de comandos de voz e para mostrar e ocultar o caractere.</span><span class="sxs-lookup"><span data-stu-id="2a244-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="2a244-111">Quando definido como **false**, o Agent desabilita qualquer parâmetro de voz para esses comandos, bem como os parâmetros de voz para a [**legenda**](caption-property.md) dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) do outro cliente.</span><span class="sxs-lookup"><span data-stu-id="2a244-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="2a244-112">Isso permite que você os elimine da gramática ativa atual do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="2a244-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="2a244-113">No entanto, como isso potencialmente bloqueia o acesso de voz a outros clientes, redefina essa propriedade como **true** depois de processar a entrada de voz do usuário.</span><span class="sxs-lookup"><span data-stu-id="2a244-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="2a244-114">Desabilitar a propriedade não afeta o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="2a244-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="2a244-115">Os comandos globais adicionados pelo servidor ainda serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="2a244-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="2a244-116">Você não pode removê-los do menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="2a244-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a244-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2a244-117">See Also</span></span>

[<span data-ttu-id="2a244-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2a244-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 