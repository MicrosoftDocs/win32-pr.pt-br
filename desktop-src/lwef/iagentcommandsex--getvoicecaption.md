---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105791361"
---
# <a name="iagentcommandsexgetvoicecaption"></a><span data-ttu-id="47bb5-103">IAgentCommandsEx::GetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="47bb5-103">IAgentCommandsEx::GetVoiceCaption</span></span>

<span data-ttu-id="47bb5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47bb5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

<span data-ttu-id="47bb5-105">Recupera o [**VoiceCaption**](voicecaption-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="47bb5-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="47bb5-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47bb5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="47bb5-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="47bb5-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="47bb5-108">O endereço de um BSTR que recebe o valor do texto de [**legenda**](caption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="47bb5-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="47bb5-109">O texto retornado é definido para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) e aparece na janela comandos de voz quando o aplicativo cliente é de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="47bb5-109">The text returned is that set for your [**Command**](/windows/desktop/lwef/the-command-object) object and appears in the Voice Commands window when your client application is input-active.</span></span>

<span data-ttu-id="47bb5-110">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="47bb5-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="47bb5-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="47bb5-111">See Also</span></span>

[<span data-ttu-id="47bb5-112">**IAgentCommandsEx::SetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="47bb5-112">**IAgentCommandsEx::SetVoiceCaption**</span></span>](iagentcommandsex--setvoicecaption.md)


 

 