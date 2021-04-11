---
title: Apêndice C IAccessible DISPIDs
description: Um DISPID permite a implementação do IDispatch para pesquisar os vários métodos e propriedades de uma interface dupla.
ms.assetid: 3d19b37a-1ce4-4f34-96b3-ff39b320e8db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d510fac39209cdb268a7676b49bbb6424cae1b09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159849"
---
# <a name="appendix-c-iaccessible-dispids"></a><span data-ttu-id="392df-103">Apêndice C: DISPIDs do IAccessible</span><span class="sxs-lookup"><span data-stu-id="392df-103">Appendix C: IAccessible DISPIDs</span></span>

<span data-ttu-id="392df-104">Um DISPID permite a implementação do [**IDispatch**](idispatch-interface.md) para pesquisar os vários métodos e propriedades de uma interface dupla.</span><span class="sxs-lookup"><span data-stu-id="392df-104">A DISPID allows the implementation of the [**IDispatch**](idispatch-interface.md) to look up the various methods and properties of a dual interface.</span></span>


```C++
// PROPERTIES: Hierarchical 
#define DISPID_ACC_PARENT                   (-5000)
#define DISPID_ACC_CHILDCOUNT               (-5001)
#define DISPID_ACC_CHILD                    (-5002)
                                             
// PROPERTIES: Descriptive 
#define DISPID_ACC_NAME                     (-5003)
#define DISPID_ACC_VALUE                    (-5004)
#define DISPID_ACC_DESCRIPTION              (-5005)
#define DISPID_ACC_ROLE                     (-5006)
#define DISPID_ACC_STATE                    (-5007)
#define DISPID_ACC_HELP                     (-5008)
#define DISPID_ACC_HELPTOPIC                (-5009)
#define DISPID_ACC_KEYBOARDSHORTCUT         (-5010)
#define DISPID_ACC_FOCUS                    (-5011)
#define DISPID_ACC_SELECTION                (-5012)
#define DISPID_ACC_DEFAULTACTION            (-5013)

// METHODS 
#define DISPID_ACC_SELECT                   (-5014)
#define DISPID_ACC_LOCATION                 (-5015)
#define DISPID_ACC_NAVIGATE                 (-5016)
#define DISPID_ACC_HITTEST                  (-5017)
#define DISPID_ACC_DODEFAULTACTION          (-5018)
```



 

 




