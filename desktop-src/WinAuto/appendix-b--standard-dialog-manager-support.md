---
title: Apêndice B suporte do Gerenciador de diálogo padrão
description: O Microsoft Acessibilidade Ativa fornece suporte completo para controles da caixa de diálogo do SDM (Gerenciador de caixas de diálogo padrão).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636024"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="15fa0-103">Apêndice B: suporte padrão do Gerenciador de diálogo</span><span class="sxs-lookup"><span data-stu-id="15fa0-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="15fa0-104">O Microsoft Acessibilidade Ativa fornece suporte completo para controles da caixa de diálogo do SDM (Gerenciador de caixas de diálogo padrão).</span><span class="sxs-lookup"><span data-stu-id="15fa0-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="15fa0-105">O SDM é uma biblioteca de código interna da Microsoft que fornece aos aplicativos da Microsoft um grau de independência das diferenças entre os sistemas operacionais Macintosh e Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="15fa0-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="15fa0-106">O SDM é usado principalmente para caixas de diálogo no Microsoft Excel e no Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="15fa0-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="15fa0-107">O SDM apresenta problemas de auxílios de acessibilidade porque usa implementações não padrão de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15fa0-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="15fa0-108">Por exemplo, os botões da caixa de diálogo SDM não usam o identificador da janela da mesma forma que os elementos da interface do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="15fa0-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="15fa0-109">Não é possível enviar mensagens para botões e botões não contidos na lista de janelas.</span><span class="sxs-lookup"><span data-stu-id="15fa0-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="15fa0-110">Um aplicativo que usa o SDM se comunica com o controle por meio de uma interface privada.</span><span class="sxs-lookup"><span data-stu-id="15fa0-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="15fa0-111">A ilustração a seguir mostra uma caixa de diálogo de exemplo do Word.</span><span class="sxs-lookup"><span data-stu-id="15fa0-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="15fa0-112">Embora pareça uma caixa de diálogo normal do Windows que usa o controle guia, é realmente uma caixa de diálogo SDM.</span><span class="sxs-lookup"><span data-stu-id="15fa0-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![captura de tela da caixa de diálogo opções com a guia Exibir selecionada](images/dialog.gif)

 

 




