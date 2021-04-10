---
title: Container-Specific interfaces privadas
description: Container-Specific interfaces privadas
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292779"
---
# <a name="container-specific-private-interfaces"></a><span data-ttu-id="39955-103">Container-Specific interfaces privadas</span><span class="sxs-lookup"><span data-stu-id="39955-103">Container-Specific Private Interfaces</span></span>

<span data-ttu-id="39955-104">Alguns contêineres fornecem interfaces privadas específicas de contêiner para funcionalidade adicional ou desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="39955-104">Some containers provide container-specific private interfaces for additional functionality or improved performance.</span></span> <span data-ttu-id="39955-105">Os controles que dependem dessas interfaces específicas de contêiner devem, se possível, funcionar sem essas interfaces específicas de contêiner presentes para que o controle funcione em diferentes contêineres.</span><span class="sxs-lookup"><span data-stu-id="39955-105">Controls that rely on those container-specific interfaces should, if possible, work without those container-specific interfaces present so that the control functions in different containers.</span></span> <span data-ttu-id="39955-106">Por exemplo, Visual Basic implementa interfaces privadas que fornecem funcionalidade de formatação de cadeia de caracteres a controles.</span><span class="sxs-lookup"><span data-stu-id="39955-106">For example, Visual Basic implements private interfaces that provide string formatting functionality to controls.</span></span> <span data-ttu-id="39955-107">Se um controle usa essas interfaces de formatação privada, ele deve ser capaz de executar com suporte de formatação padrão se essas interfaces não estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="39955-107">If a control makes use of these private formatting interfaces, it should be able to run with default formatting support if these interfaces are not available.</span></span> <span data-ttu-id="39955-108">Se o controle puder funcionar sem as interfaces privadas, ele deverá executar a ação apropriada (como avisar o usuário sobre a funcionalidade reduzida), mas continuar a trabalhar.</span><span class="sxs-lookup"><span data-stu-id="39955-108">If the control can function without the private interfaces, it should take appropriate action (such as warn the user of reduced functionality) but continue to work.</span></span> <span data-ttu-id="39955-109">Se essa não for uma opção, uma categoria de componente deverá ser registrada conforme necessário para que somente os contêineres que dão suporte a essa funcionalidade possam hospedar esses controles.</span><span class="sxs-lookup"><span data-stu-id="39955-109">If this is not an option, a component category should be registered as required so that only containers supporting this functionality can host these controls.</span></span>

 

 




