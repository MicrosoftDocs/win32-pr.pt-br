---
title: Automação de Acessibilidade Ativa e interface do usuário
description: O Microsoft Acessibilidade Ativa foi projetado para uso com o Windows XP e sistemas operacionais anteriores.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796198"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="fa664-103">Automação de Acessibilidade Ativa e interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fa664-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="fa664-104">O Microsoft Acessibilidade Ativa foi projetado para uso com o Windows XP e sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="fa664-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="fa664-105">Os desenvolvedores de controles personalizados e aplicativos cliente de tecnologia acessível para Windows XP e Windows Vista devem considerar o uso [da automação da interface do usuário da](entry-uiauto-win32.md) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa664-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="fa664-106">O Microsoft UI Automation é um sistema completo que fornece informações mais precisas sobre a interface do usuário e dá ao usuário mais capacidade para interagir com controles.</span><span class="sxs-lookup"><span data-stu-id="fa664-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="fa664-107">Em particular, ele fornece suporte muito aprimorado para texto.</span><span class="sxs-lookup"><span data-stu-id="fa664-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="fa664-108">Um conjunto de objetos proxy fornece suporte à automação da interface do usuário para controles padrão do Microsoft Win32 e Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="fa664-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="fa664-109">O suporte mais rico está disponível para controles especificamente escritos com a automação da interface do usuário em mente, incluindo elementos nativos do Windows Presentation Foundation (WPF), que não oferecem suporte direto ao Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="fa664-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="fa664-110">Controles personalizados que dão suporte à automação da interface do usuário podem ser escritos em código gerenciado ou não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fa664-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="fa664-111">Os clientes Microsoft Acessibilidade Ativa têm acesso limitado, por meio de uma camada de pontes, a elementos da interface do usuário que dão suporte apenas à automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fa664-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="fa664-112">Para obter mais informações, consulte o [Apêndice G: acessibilidade ativa ponte à automação da interface do usuário](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span><span class="sxs-lookup"><span data-stu-id="fa664-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="fa664-113">Para obter mais informações sobre as semelhanças e diferenças entre o Microsoft Acessibilidade Ativa e a automação da interface do usuário, consulte [microsoft acessibilidade ativa e automação da interface do usuário em comparação](microsoft-active-accessibility-and-ui-automation-compared.md).</span><span class="sxs-lookup"><span data-stu-id="fa664-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa664-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa664-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fa664-115">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="fa664-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fa664-116">Introdução</span><span class="sxs-lookup"><span data-stu-id="fa664-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="fa664-117">Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="fa664-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




