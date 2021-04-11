---
title: Manipulação de teclado para controles
description: Um controle responde aos aceleradores de teclado para que o usuário final possa iniciar ações executadas pelo controle.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292813"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="57cd0-103">Manipulação de teclado para controles</span><span class="sxs-lookup"><span data-stu-id="57cd0-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="57cd0-104">Um controle responde aos aceleradores de teclado para que o usuário final possa iniciar ações executadas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="57cd0-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="57cd0-105">O contêiner gerencia a atividade de teclado para todos os seus controles inseridos.</span><span class="sxs-lookup"><span data-stu-id="57cd0-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="57cd0-106">Com documentos compostos, os aceleradores de teclado se aplicam somente ao objeto ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="57cd0-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="57cd0-107">Com controles, um mecanismo foi adicionado para que um controle possa responder a seus mnemônicos de teclado, mesmo que ele não esteja atualmente na interface do usuário-ativo.</span><span class="sxs-lookup"><span data-stu-id="57cd0-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="57cd0-108">Os métodos [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemônico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) e o método [**IOleControlSite:: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) manipulam os mnemônicos de teclado de um controle.</span><span class="sxs-lookup"><span data-stu-id="57cd0-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="57cd0-109">Uma estrutura [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) descreve os aceleradores mnemônicos de um controle e os sinalizadores passados com ele por meio do método **GetControlInfo** descrevem o comportamento dos controles com as teclas ENTER e ESC.</span><span class="sxs-lookup"><span data-stu-id="57cd0-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="57cd0-110">Quando um controle altera seus mnemônicos, ele chama **OnControlInfoChanged** para que o contêiner possa recarregar a estrutura, se necessário.</span><span class="sxs-lookup"><span data-stu-id="57cd0-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="57cd0-111">Quando um controle está ativo na interface do usuário, ele também é o controle com o foco.</span><span class="sxs-lookup"><span data-stu-id="57cd0-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="57cd0-112">Como os controles são ativados e desativados entre o ativo in-loco e os Estados ativos da interface do usuário, o controle chama [**IOleControlSite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) para informar ao contêiner de tais alterações.</span><span class="sxs-lookup"><span data-stu-id="57cd0-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="57cd0-113">Além disso, quando um controle está ativo na interface do usuário, ele terá a primeira chance de processar qualquer pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="57cd0-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="57cd0-114">Para dar a um contêiner a oportunidade de processar o pressionamento de tecla antes do controle, o controle chama [**IOleControlSite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span><span class="sxs-lookup"><span data-stu-id="57cd0-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="57cd0-115">Se o contêiner não tratar o pressionamento de tecla, o controle o processará.</span><span class="sxs-lookup"><span data-stu-id="57cd0-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57cd0-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57cd0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57cd0-117">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="57cd0-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




