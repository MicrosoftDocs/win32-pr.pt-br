---
description: Os provedores WMI são geralmente projetados para fornecer informações sobre um objeto gerenciado específico em um único computador.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Vinculando classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794613"
---
# <a name="linking-classes-together"></a><span data-ttu-id="498a3-103">Vinculando classes</span><span class="sxs-lookup"><span data-stu-id="498a3-103">Linking Classes Together</span></span>

<span data-ttu-id="498a3-104">Os provedores WMI são geralmente projetados para fornecer informações sobre um objeto gerenciado específico em um único computador.</span><span class="sxs-lookup"><span data-stu-id="498a3-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="498a3-105">Se houver uma propriedade comum que possa servir como uma chave para identificar exclusivamente todas as instâncias de origem diferentes, use o provedor de [exibição](view-provider.md) para combinar Propriedades de diferentes classes, namespaces ou computadores em uma única classe.</span><span class="sxs-lookup"><span data-stu-id="498a3-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="498a3-106">Primeiro, você deve [registrar o provedor de exibição](registering-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="498a3-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="498a3-107">Após o registro, você pode criar os seguintes tipos de classes de exibição:</span><span class="sxs-lookup"><span data-stu-id="498a3-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="498a3-108">Modo de exibição de junção</span><span class="sxs-lookup"><span data-stu-id="498a3-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="498a3-109">Instâncias de classes diferentes conectadas por um valor de propriedade comum.</span><span class="sxs-lookup"><span data-stu-id="498a3-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="498a3-110">Exibição de associação</span><span class="sxs-lookup"><span data-stu-id="498a3-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="498a3-111">Exibições de classes de associação existentes no limite do namespace.</span><span class="sxs-lookup"><span data-stu-id="498a3-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="498a3-112">Exibição de União</span><span class="sxs-lookup"><span data-stu-id="498a3-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="498a3-113">União de uma ou mais instâncias.</span><span class="sxs-lookup"><span data-stu-id="498a3-113">Union of one or more instances.</span></span>

 

 



