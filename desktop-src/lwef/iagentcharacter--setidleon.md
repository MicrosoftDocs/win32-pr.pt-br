---
title: IAgentCharacter setocioso
description: IAgentCharacter setocioso
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364496"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="178c7-103">IAgentCharacter:: setidleion</span><span class="sxs-lookup"><span data-stu-id="178c7-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="178c7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="178c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="178c7-105">Define o processamento de ociosidade automático para um caractere.</span><span class="sxs-lookup"><span data-stu-id="178c7-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="178c7-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="178c7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="178c7-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bno*</span><span class="sxs-lookup"><span data-stu-id="178c7-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="178c7-108">Sinalizador de processamento ocioso.</span><span class="sxs-lookup"><span data-stu-id="178c7-108">Idle processing flag.</span></span> <span data-ttu-id="178c7-109">Se esse parâmetro for **true**, o Microsoft Agent reproduzirá automaticamente animações de estado **deixar** .</span><span class="sxs-lookup"><span data-stu-id="178c7-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="178c7-110">O servidor define automaticamente um tempo limite após a última animação executada para um caractere.</span><span class="sxs-lookup"><span data-stu-id="178c7-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="178c7-111">Quando o intervalo desse temporizador for concluído, o servidor começará os Estados **deixar** de um caractere, jogando suas animações **deixar** associadas em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="178c7-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="178c7-112">Se você quiser gerenciar as animações de estado **deixar** por conta própria, defina a propriedade como **false**.</span><span class="sxs-lookup"><span data-stu-id="178c7-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="178c7-113">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="178c7-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="178c7-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="178c7-114">See Also</span></span>

[<span data-ttu-id="178c7-115">**IAgentCharacter:: getidley**</span><span class="sxs-lookup"><span data-stu-id="178c7-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




