---
title: Confinamento de site de quadro simples
description: Confinamento de site de quadro simples
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916125"
---
# <a name="simple-frame-site-containment"></a><span data-ttu-id="dd711-103">Confinamento de site de quadro simples</span><span class="sxs-lookup"><span data-stu-id="dd711-103">Simple Frame Site Containment</span></span>

<span data-ttu-id="dd711-104">Um controle de contêiner é um controle ActiveX capaz de conter outros controles.</span><span class="sxs-lookup"><span data-stu-id="dd711-104">A container control is an ActiveX control that is capable of containing other controls.</span></span> <span data-ttu-id="dd711-105">Uma caixa de grupo que contém uma coleção de botões de opção é um exemplo de um controle de contêiner.</span><span class="sxs-lookup"><span data-stu-id="dd711-105">A group box that contains a collection of radio buttons is an example of a container control.</span></span> <span data-ttu-id="dd711-106">Os controles de contêiner devem definir o \_ bit de status OLEMISC SIMPLEFRAME e devem chamar a implementação de [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dd711-106">Container controls should set the OLEMISC\_SIMPLEFRAME status bit, and should call its container's [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementation.</span></span> <span data-ttu-id="dd711-107">Um contêiner de controle ActiveX que dá suporte a controles de contêiner deve implementar **ISimpleFrameSite**.</span><span class="sxs-lookup"><span data-stu-id="dd711-107">An ActiveX control container that supports container controls must implement **ISimpleFrameSite**.</span></span>

<span data-ttu-id="dd711-108">CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl</span><span class="sxs-lookup"><span data-stu-id="dd711-108">CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID\_SimpleFrameControl</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd711-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd711-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd711-110">Categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="dd711-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




