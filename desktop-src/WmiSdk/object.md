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

 

 



