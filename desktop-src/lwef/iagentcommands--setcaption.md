---
title: IAgentCommands AutoCaption
description: IAgentCommands AutoCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365874"
---
# <a name="iagentcommandssetcaption"></a><span data-ttu-id="e655e-103">IAgentCommands:: SetCaption</span><span class="sxs-lookup"><span data-stu-id="e655e-103">IAgentCommands::SetCaption</span></span>

<span data-ttu-id="e655e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e655e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

<span data-ttu-id="e655e-105">Define o texto de [**legenda**](caption-property.md) exibido para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e655e-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e655e-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e655e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e655e-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="e655e-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="e655e-108">Um BSTR que especifica o valor da propriedade [**Caption**](caption-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e655e-108">A BSTR that specifies the value for the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="e655e-109">Definir a propriedade [**Caption**](caption-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) define como ela será exibida no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) é definida como **true** e seu aplicativo não é o cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="e655e-109">Setting the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="e655e-110">Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere.</span><span class="sxs-lookup"><span data-stu-id="e655e-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="e655e-111">Se você definir comandos para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tenha sua [**legenda**](caption-property.md) definida, normalmente também definirá uma **legenda** para sua coleção de **comandos** .</span><span class="sxs-lookup"><span data-stu-id="e655e-111">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has its [**Caption**](caption-property.md) set, you typically also define a **Caption** for its **Commands** collection.</span></span>

## <a name="see-also"></a><span data-ttu-id="e655e-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e655e-112">See Also</span></span>

<span data-ttu-id="e655e-113">[**IAgentCommands:: getCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: setvisível**](iagentcommands--setvisible.md), [**IAgentCommands:: setvoice**](iagentcommands--setvoice.md)</span><span class="sxs-lookup"><span data-stu-id="e655e-113">[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)</span></span>


 

 