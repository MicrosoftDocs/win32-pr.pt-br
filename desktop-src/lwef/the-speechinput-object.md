---
title: O objeto SpeechInput
description: O objeto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916426"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="996c7-103">O objeto SpeechInput</span><span class="sxs-lookup"><span data-stu-id="996c7-103">The SpeechInput Object</span></span>

<span data-ttu-id="996c7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="996c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="996c7-105">O objeto [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fornece acesso às propriedades de entrada de fala mantidas pelo servidor do agente.</span><span class="sxs-lookup"><span data-stu-id="996c7-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="996c7-106">As propriedades são somente leitura para aplicativos cliente, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="996c7-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="996c7-107">O servidor retornará valores somente se um mecanismo de fala compatível tiver sido instalado e estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="996c7-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="996c7-108">As propriedades [**Engine**](https://www.bing.com/search?q=**Engine**), [**installed**](https://www.bing.com/search?q=**Installed**)e [**Language**](https://www.bing.com/search?q=**Language**) não têm mais suporte, mas (para compatibilidade com versões anteriores) retornarão valores nulos se consultados.</span><span class="sxs-lookup"><span data-stu-id="996c7-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="996c7-109">Para consultar ou definir o modo de reconhecimento de fala, use a propriedade [**SRModeID**](srmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="996c7-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="996c7-110">Propriedades de SpeechInput</span><span class="sxs-lookup"><span data-stu-id="996c7-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 




