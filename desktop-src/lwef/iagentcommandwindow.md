---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765713"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="c8ba3-103">IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="c8ba3-103">IAgentCommandWindow</span></span>

<span data-ttu-id="c8ba3-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8ba3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c8ba3-105">**IAgentCommandWindow** define uma interface que permite que os aplicativos definam e consultem as propriedades da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="c8ba3-106">A janela de comandos de voz é um recurso compartilhado projetado principalmente para permitir que os usuários exibam comandos habilitados para voz.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="c8ba3-107">Se o reconhecimento de fala estiver desabilitado, a janela comandos de voz ainda será exibida, com o texto "entrada de fala desabilitada" (no idioma do caractere).</span><span class="sxs-lookup"><span data-stu-id="c8ba3-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="c8ba3-108">Se nenhum mecanismo de fala estiver instalado que corresponda à configuração de idioma do caractere, a janela será exibida, "entrada de fala não disponível".</span><span class="sxs-lookup"><span data-stu-id="c8ba3-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="c8ba3-109">Se o cliente de entrada-ativo não tiver definido parâmetros de voz para seus comandos e tiver desabilitado os comandos de voz globais, a janela exibirá "nenhum comando de voz".</span><span class="sxs-lookup"><span data-stu-id="c8ba3-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="c8ba3-110">Você também pode consultar as propriedades da janela de comandos de voz independentemente se a entrada de fala está desabilitada ou se um mecanismo de fala compatível está instalado.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="c8ba3-111">**Métodos em ordem vtable**</span><span class="sxs-lookup"><span data-stu-id="c8ba3-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="c8ba3-112">Métodos IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="c8ba3-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="c8ba3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8ba3-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8ba3-114">**Não visível**</span><span class="sxs-lookup"><span data-stu-id="c8ba3-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="c8ba3-115">Define o valor da propriedade [**Visible**](visible-property.md) da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="c8ba3-116">**GetVisible**</span><span class="sxs-lookup"><span data-stu-id="c8ba3-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="c8ba3-117">Retorna o valor da propriedade [**Visible**](visible-property.md) da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="c8ba3-118">**GetPosition**</span><span class="sxs-lookup"><span data-stu-id="c8ba3-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="c8ba3-119">Retorna a posição da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="c8ba3-120">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="c8ba3-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="c8ba3-121">Retorna o tamanho da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c8ba3-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 




