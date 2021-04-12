---
title: Acessibilidade de controle ActiveX sem janela
description: Esta seção descreve como usar a API de acessibilidade do Windows para garantir que os controles ActiveX sem janela do Microsoft estejam acessíveis.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366403"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="b3541-103">Acessibilidade de controle ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="b3541-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="b3541-104">Esta seção descreve como usar a API de acessibilidade do Windows para garantir que os controles ActiveX sem janela do Microsoft estejam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="b3541-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="b3541-105">O Windows 8 inclui novas interfaces de API de acessibilidade do Windows que simplificam a tarefa de implementar a acessibilidade para controles ActiveX sem janela.</span><span class="sxs-lookup"><span data-stu-id="b3541-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="b3541-106">A API inclui interfaces que são implementadas em um controle sem janela e no contêiner de controle, permitindo que o controle sem janela e seu contêiner funcionem juntos para fornecer informações de acessibilidade sobre o controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="b3541-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="b3541-107">A API dá suporte aos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="b3541-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="b3541-108">Controles do Microsoft Acessibilidade Ativa sem janela hospedados em um contêiner de controle do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="b3541-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="b3541-109">Controles do Microsoft Acessibilidade Ativa sem janela hospedados em um contêiner de controle de automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3541-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="b3541-110">Controles sem janela de automação da interface do usuário hospedados em um contêiner de controle do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="b3541-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="b3541-111">Controles sem janela de automação da interface do usuário hospedados em um contêiner de controle de automação de interface</span><span class="sxs-lookup"><span data-stu-id="b3541-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="b3541-112">A tabela a seguir lista as interfaces que dão suporte a controles ActiveX sem janelas e identifica os objetos que implementam as interfaces.</span><span class="sxs-lookup"><span data-stu-id="b3541-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="b3541-113">Objeto</span><span class="sxs-lookup"><span data-stu-id="b3541-113">Object</span></span>              | <span data-ttu-id="b3541-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="b3541-114">MSAA</span></span>                                                                             | <span data-ttu-id="b3541-115">Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="b3541-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3541-116">Objeto de controle</span><span class="sxs-lookup"><span data-stu-id="b3541-116">Control object</span></span>      | [<span data-ttu-id="b3541-117">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="b3541-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="b3541-118">Site de controle</span><span class="sxs-lookup"><span data-stu-id="b3541-118">Control site</span></span>        | [<span data-ttu-id="b3541-119">**IAccessibleWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="b3541-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="b3541-120">**IRawElementProviderWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="b3541-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="b3541-121">Raiz da janela do host</span><span class="sxs-lookup"><span data-stu-id="b3541-121">Root of host window</span></span> | [<span data-ttu-id="b3541-122">**IAccessibleHostingElementProviders**</span><span class="sxs-lookup"><span data-stu-id="b3541-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="b3541-123">**IRawElementProviderHostingAccessibles**</span><span class="sxs-lookup"><span data-stu-id="b3541-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="b3541-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b3541-124">In this section</span></span>

-   [<span data-ttu-id="b3541-125">Como usar a automação da interface do usuário para tornar um controle ActiveX sem janela acessível</span><span class="sxs-lookup"><span data-stu-id="b3541-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="b3541-126">Como usar a MSAA para tornar um controle ActiveX sem janela acessível</span><span class="sxs-lookup"><span data-stu-id="b3541-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="b3541-127">Como hospedar um controle ActiveX sem janela de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="b3541-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="b3541-128">Como hospedar um controle ActiveX sem janela do MSAA</span><span class="sxs-lookup"><span data-stu-id="b3541-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 