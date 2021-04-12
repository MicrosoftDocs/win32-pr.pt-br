---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363622"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="f2f1d-103">IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="f2f1d-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="f2f1d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f2f1d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f2f1d-105">O IAgentSpeechInputProperties fornece acesso às propriedades de entrada de fala mantidas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="f2f1d-106">A maioria das propriedades é somente leitura para aplicativos cliente, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="f2f1d-107">O servidor do Microsoft Agent retornará valores somente se um mecanismo de fala compatível tiver sido instalado e estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="f2f1d-108">A consulta dessas propriedades tenta iniciar o mecanismo de fala.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="f2f1d-109">**Métodos em ordem vtable**</span><span class="sxs-lookup"><span data-stu-id="f2f1d-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="f2f1d-110">Métodos IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="f2f1d-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="f2f1d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f1d-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="f2f1d-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="f2f1d-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="f2f1d-113">Retorna se o mecanismo de reconhecimento de fala está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="f2f1d-114">**Gettecla de atalho**</span><span class="sxs-lookup"><span data-stu-id="f2f1d-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="f2f1d-115">Retorna a atribuição de chave atual da chave de escuta.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="f2f1d-116">**GetListeningTip**</span><span class="sxs-lookup"><span data-stu-id="f2f1d-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="f2f1d-117">Retorna se a dica de escuta está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="f2f1d-118">Os métodos [**Getinstaled**](https://www.bing.com/search?q=**GetInstalled**), [**getlcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)e [**setengine**](https://www.bing.com/search?q=**SetEngine**) (com suporte em versões anteriores do Microsoft Agent) ainda têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="f2f1d-119">No entanto, os métodos não são fragmentado e não retornam valores úteis.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="f2f1d-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) e [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) para consultar e definir o mecanismo de reconhecimento de fala a ser usado com o caractere.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="f2f1d-121">Tenha em mente que o mecanismo deve corresponder à configuração de idioma atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 




