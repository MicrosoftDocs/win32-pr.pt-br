---
description: O tipo de dados OBJECT é um objeto de classe WMI usado para declarar associações de tipo fraco e objetos incorporados.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c26b8b6ff77f788aeed607057541d19d80fea4c105b53d492c1f1e8468b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554925"
---
# <a name="object"></a>OBJECT

O tipo de dados OBJECT é um objeto de classe WMI usado para declarar associações de tipo fraco e objetos incorporados. Você não define a classe específica para um objeto de tipo fraco até criar uma instância da classe. Os objetos inseridos definidos com o tipo de dados objeto podem conter instâncias de qualquer classe WMI. Para obter mais informações, consulte [objetos incorporados](embedded-objects.md).

O exemplo a seguir define e cria instâncias de duas classes, uma das quais contém um objeto incorporado do tipo OBJECT:

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

 

 



