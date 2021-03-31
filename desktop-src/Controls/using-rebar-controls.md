---
title: Usando controles Rebar
description: Esta seção contém tópicos que demonstram como criar e usar controles Rebar.
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641901"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="c8a17-103">Usando controles Rebar</span><span class="sxs-lookup"><span data-stu-id="c8a17-103">Using Rebar Controls</span></span>

<span data-ttu-id="c8a17-104">Esta seção contém tópicos que demonstram como criar e usar controles Rebar.</span><span class="sxs-lookup"><span data-stu-id="c8a17-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c8a17-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c8a17-105">In this section</span></span>



| <span data-ttu-id="c8a17-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="c8a17-106">Topic</span></span>                                                                | <span data-ttu-id="c8a17-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8a17-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8a17-108">Como criar controles Rebar</span><span class="sxs-lookup"><span data-stu-id="c8a17-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="c8a17-109">Um aplicativo cria um controle rebar chamando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando [**REBARCLASSNAME**](common-control-window-classes.md) como a classe Window.</span><span class="sxs-lookup"><span data-stu-id="c8a17-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="c8a17-110">O aplicativo deve primeiro registrar a classe de janela chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando o \_ bit de classes legais ICC \_ na estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="c8a17-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

