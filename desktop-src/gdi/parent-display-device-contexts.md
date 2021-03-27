---
description: Um contexto de dispositivo pai permite que um aplicativo minimize o tempo necessário para configurar a região de recorte para uma janela.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Os contextos do dispositivo de exibição pai
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967623"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="3459b-103">Os contextos do dispositivo de exibição pai</span><span class="sxs-lookup"><span data-stu-id="3459b-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="3459b-104">Um *contexto de dispositivo pai* permite que um aplicativo minimize o tempo necessário para configurar a região de recorte para uma janela.</span><span class="sxs-lookup"><span data-stu-id="3459b-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="3459b-105">Um aplicativo normalmente usa contextos de dispositivo pai para acelerar o desenho de janelas de controle sem a necessidade de um contexto de dispositivo privado ou de classe.</span><span class="sxs-lookup"><span data-stu-id="3459b-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="3459b-106">Por exemplo, o sistema usa contextos de dispositivo pai para botão de ação e controles de edição.</span><span class="sxs-lookup"><span data-stu-id="3459b-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="3459b-107">Os contextos de dispositivo pai destinam-se ao uso somente com janelas filhas, nunca com janelas de nível superior ou pop-up.</span><span class="sxs-lookup"><span data-stu-id="3459b-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="3459b-108">Um aplicativo pode especificar o \_ estilo cs PARENTDC para definir a região de recorte da janela filho para a da janela pai, de forma que o filho possa desenhar no pai.</span><span class="sxs-lookup"><span data-stu-id="3459b-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="3459b-109">A especificação do CS \_ PARENTDC aprimora o desempenho de um aplicativo porque o sistema não precisa continuar recalculando a região visível para cada janela filho.</span><span class="sxs-lookup"><span data-stu-id="3459b-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="3459b-110">Os valores de atributo definidos pela janela pai não são preservados para a janela filho; por exemplo, a janela pai não pode definir o pincel para suas janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="3459b-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="3459b-111">A única propriedade preservada é a região de recorte.</span><span class="sxs-lookup"><span data-stu-id="3459b-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="3459b-112">A janela deve cortar sua própria saída nos limites da janela.</span><span class="sxs-lookup"><span data-stu-id="3459b-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="3459b-113">Como a região de recorte para o contexto do dispositivo pai é idêntica à janela pai, a janela filho pode potencialmente desenhar sobre toda a janela pai, mas o contexto do dispositivo pai não deve ser usado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="3459b-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="3459b-114">O sistema ignorará o \_ estilo cs PARENTDC se a janela pai usar um contexto de dispositivo privado ou de classe, se a janela pai cortar suas janelas filhas ou se a janela filho cortar suas janelas filhas ou irmãs.</span><span class="sxs-lookup"><span data-stu-id="3459b-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 



