---
title: Controles do Windows
description: Um controle é uma janela filho que um aplicativo usa em conjunto com outra janela para habilitar a interação do usuário.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005123"
---
# <a name="windows-controls"></a><span data-ttu-id="31831-103">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="31831-103">Windows Controls</span></span>

## <a name="purpose"></a><span data-ttu-id="31831-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="31831-104">Purpose</span></span>

<span data-ttu-id="31831-105">Um controle é uma janela filho que um aplicativo usa em conjunto com outra janela para habilitar a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="31831-105">A control is a child window that an application uses in conjunction with another window to enable user interaction.</span></span> <span data-ttu-id="31831-106">Os controles são usados com mais frequência nas caixas de diálogo, mas também podem ser usados em outras janelas.</span><span class="sxs-lookup"><span data-stu-id="31831-106">Controls are most often used within dialog boxes, but they can also be used in other windows.</span></span> <span data-ttu-id="31831-107">Os controles nas caixas de diálogo fornecem ao usuário uma maneira de digitar texto, escolher opções e iniciar ações.</span><span class="sxs-lookup"><span data-stu-id="31831-107">Controls within dialog boxes provide the user with a way to type text, choose options, and initiate actions.</span></span> <span data-ttu-id="31831-108">Os controles em outras janelas fornecem uma variedade de serviços, como permitir que o usuário escolha comandos, Exibir status e exibir e editar texto.</span><span class="sxs-lookup"><span data-stu-id="31831-108">Controls in other windows provide a variety of services, such as letting the user choose commands, view status, and view and edit text.</span></span> <span data-ttu-id="31831-109">Esta documentação descreve os controles fornecidos pelo Windows e os elementos de programação usados para criá-los e manipulá-los.</span><span class="sxs-lookup"><span data-stu-id="31831-109">This documentation describes the controls provided by Windows and the programming elements used to create and manipulate them.</span></span>

<span data-ttu-id="31831-110">Para obter uma lista de todos os controles do Windows, incluindo um link para uma visão geral abrangente e informações de referência para cada controle, consulte [Control library](individual-control-info.md).</span><span class="sxs-lookup"><span data-stu-id="31831-110">For a list of all Windows controls, including a link to comprehensive overview and reference information for each control, see [Control Library](individual-control-info.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="31831-111">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="31831-111">Developer audience</span></span>

<span data-ttu-id="31831-112">Os controles são projetados para uso por desenvolvedores de C/C++ e designers de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="31831-112">Controls are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="31831-113">Em geral, os desenvolvedores precisam de um nível moderado de compreensão sobre conceitos de programação de interface do usuário, programação de API do Windows e Unicode.</span><span class="sxs-lookup"><span data-stu-id="31831-113">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="31831-114">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="31831-114">Run-time requirements</span></span>

<span data-ttu-id="31831-115">O suporte para controles é fornecido por User32.dll e Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="31831-115">Support for controls is provided by User32.dll and Comctl32.dll.</span></span> <span data-ttu-id="31831-116">Para obter mais informações, consulte [versões de controle comuns](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="31831-116">For more information, see [Common Control Versions](common-control-versions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="31831-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="31831-117">In this section</span></span>



| <span data-ttu-id="31831-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="31831-118">Topic</span></span>                                                                             | <span data-ttu-id="31831-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="31831-119">Description</span></span>                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31831-120">Sobre controles comuns</span><span class="sxs-lookup"><span data-stu-id="31831-120">About Common Controls</span></span>](common-controls-intro.md)<br/>                     | <span data-ttu-id="31831-121">Fornece informações gerais que são comuns a todos os controles com suporte pelo Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="31831-121">Provides general information that is common to all controls that are supported by Comctl32.dll.</span></span><br/>                                      |
| [<span data-ttu-id="31831-122">Mensagens de controle</span><span class="sxs-lookup"><span data-stu-id="31831-122">Control Messages</span></span>](control-messages.md)<br/>                               | <span data-ttu-id="31831-123">Explica como as mensagens do Windows são usadas para se comunicar com controles.</span><span class="sxs-lookup"><span data-stu-id="31831-123">Explains how Windows messages are used to communicate with controls.</span></span><br/>                                                                 |
| [<span data-ttu-id="31831-124">Controles personalizados</span><span class="sxs-lookup"><span data-stu-id="31831-124">Custom Controls</span></span>](user-controls-intro.md)<br/>                             | <span data-ttu-id="31831-125">Descreve várias maneiras de criar controles personalizados.</span><span class="sxs-lookup"><span data-stu-id="31831-125">Describes various ways of creating custom controls.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="31831-126">Controles de subclasses</span><span class="sxs-lookup"><span data-stu-id="31831-126">Subclassing Controls</span></span>](subclassing-overview.md)<br/>                       | <span data-ttu-id="31831-127">Descreve uma maneira de personalizar um controle alterando seus recursos ou adicionando novos.</span><span class="sxs-lookup"><span data-stu-id="31831-127">Describes a way to customize a control by changing its features or adding new ones.</span></span> <br/>                                                 |
| [<span data-ttu-id="31831-128">Desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="31831-128">Custom Draw</span></span>](custom-draw.md)<br/>                                         | <span data-ttu-id="31831-129">Descreve um serviço, fornecido por alguns controles, que os aplicativos podem usar para personalizar vários aspectos da aparência do controle.</span><span class="sxs-lookup"><span data-stu-id="31831-129">Describes a service, provided by some controls, that applications can use to customize various aspects of the control's appearance.</span></span> <br/> |
| [<span data-ttu-id="31831-130">Considerações de segurança: controles do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="31831-130">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)<br/> | <span data-ttu-id="31831-131">Fornece informações sobre considerações de segurança relacionadas aos controles do Windows.</span><span class="sxs-lookup"><span data-stu-id="31831-131">Provides information about security considerations related to the Windows controls.</span></span> <br/>                                                 |
| [<span data-ttu-id="31831-132">Biblioteca de controles</span><span class="sxs-lookup"><span data-stu-id="31831-132">Control Library</span></span>](individual-control-info.md)<br/>                         | <span data-ttu-id="31831-133">Fornece visões gerais e informações de referência sobre cada controle com suporte pelo User32.dll e Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="31831-133">Provides overviews and reference information about each control supported by User32.dll and Comctl32.dll.</span></span><br/>                            |
| [<span data-ttu-id="31831-134">Referência de controle geral</span><span class="sxs-lookup"><span data-stu-id="31831-134">General Control Reference</span></span>](common-control-reference.md)<br/>              | <span data-ttu-id="31831-135">Fornece informações de referência sobre elementos de programação que se aplicam a vários controles, não apenas a um controle específico.</span><span class="sxs-lookup"><span data-stu-id="31831-135">Provides reference information about programming elements that apply to multiple controls, not just to a specific control.</span></span><br/>           |
| [<span data-ttu-id="31831-136">Controle Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="31831-136">Control Spy v2.0</span></span>](control-spy.md)<br/>                                    | <span data-ttu-id="31831-137">Descreve o Spy Control, uma ferramenta que ajuda os desenvolvedores a entenderem os controles comuns.</span><span class="sxs-lookup"><span data-stu-id="31831-137">Describes Control Spy, a tool that helps developers understand common controls.</span></span> <br/>                                                     |
| [<span data-ttu-id="31831-138">Estilos visuais</span><span class="sxs-lookup"><span data-stu-id="31831-138">Visual Styles</span></span>](themes-overview.md)<br/>                                   | <span data-ttu-id="31831-139">Descreve como a aparência dos controles pode ser alterada dependendo do estilo visual escolhido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="31831-139">Describes how the appearance of controls can change depending on the visual style chosen by the user.</span></span> <br/>                               |
| [<span data-ttu-id="31831-140">Formato de arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="31831-140">Theme File Format</span></span>](themesfileformat-overview.md)<br/>                     | <span data-ttu-id="31831-141">Discute o formato dos arquivos de tema (. Theme) usados no Windows 7 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31831-141">Discusses the format of Theme (.theme) files used in Windows 7 and Windows Vista.</span></span><br/>                                                    |



 

 

 





