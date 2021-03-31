---
description: O tipo de dados OBJECT é um objeto de classe WMI usado para declarar associações de tipo fraco e objetos incorporados.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646653"
---
# <a name="object"></a><span data-ttu-id="e5b3a-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="e5b3a-103">OBJECT</span></span>

<span data-ttu-id="e5b3a-104">O tipo de dados OBJECT é um objeto de classe WMI usado para declarar associações de tipo fraco e objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="e5b3a-105">Você não define a classe específica para um objeto de tipo fraco até criar uma instância da classe.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="e5b3a-106">Os objetos inseridos definidos com o tipo de dados objeto podem conter instâncias de qualquer classe WMI.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="e5b3a-107">Para obter mais informações, consulte [objetos incorporados](embedded-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="e5b3a-108">O exemplo a seguir define e cria instâncias de duas classes, uma das quais contém um objeto incorporado do tipo OBJECT:</span><span class="sxs-lookup"><span data-stu-id="e5b3a-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 



