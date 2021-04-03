---
title: Visual Basic interfaces privadas
description: Visual Basic interfaces privadas
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006164"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="4ec6f-103">Visual Basic interfaces privadas</span><span class="sxs-lookup"><span data-stu-id="4ec6f-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="4ec6f-104">Duas interfaces implementadas por Visual Basic são identificadas aqui para categorias de componentes.</span><span class="sxs-lookup"><span data-stu-id="4ec6f-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="4ec6f-105">Não é esperado que os controles exijam essas categorias porque é possível que os controles ofereçam funcionalidade alternativa quando não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4ec6f-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="4ec6f-106">A interface [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permite que os controles se integrem melhor ao ambiente de Visual Basic ao formatar dados.</span><span class="sxs-lookup"><span data-stu-id="4ec6f-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="4ec6f-107">CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat</span><span class="sxs-lookup"><span data-stu-id="4ec6f-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="4ec6f-108">A interface [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite que um controle enumere outros controles no formulário do VB.</span><span class="sxs-lookup"><span data-stu-id="4ec6f-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="4ec6f-109">CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl</span><span class="sxs-lookup"><span data-stu-id="4ec6f-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="4ec6f-110">Duas interfaces privadas adicionais, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), são descritas aqui, mesmo que não definam categorias de componentes.</span><span class="sxs-lookup"><span data-stu-id="4ec6f-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="4ec6f-111">Não é recomendável usar essas quatro interfaces porque elas não têm suporte em contêineres diferentes de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4ec6f-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ec6f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ec6f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec6f-113">Categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="4ec6f-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




