---
title: O objeto AudioOutput
description: O objeto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366010"
---
# <a name="the-audiooutput-object"></a><span data-ttu-id="52a05-103">O objeto AudioOutput</span><span class="sxs-lookup"><span data-stu-id="52a05-103">The AudioOutput Object</span></span>

<span data-ttu-id="52a05-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52a05-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="52a05-105">Esse objeto fornece acesso a propriedades de saída de áudio mantidas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52a05-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="52a05-106">As propriedades são somente leitura, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="52a05-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="52a05-107">Se você declarar uma variável de objeto do tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), não será possível acessar todas as propriedades do objeto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) .</span><span class="sxs-lookup"><span data-stu-id="52a05-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="52a05-108">Embora o Agent também dê suporte a [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), essa última interface é fornecida apenas para fins de compatibilidade com versões anteriores e dá suporte apenas a essas propriedades em versões antigas.</span><span class="sxs-lookup"><span data-stu-id="52a05-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="52a05-109">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="52a05-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="52a05-110">**SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="52a05-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="52a05-111">**Estado**</span><span class="sxs-lookup"><span data-stu-id="52a05-111">**Status**</span></span>](status-property.md)

 

 