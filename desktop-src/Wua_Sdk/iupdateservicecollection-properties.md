---
description: A interface IUpdateServiceCollection define as propriedades a seguir.
ms.assetid: 340a63ee-8e31-467d-88d2-f320ccc0f054
title: Propriedades de IUpdateServiceCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4292a128587d961447c29acf22aa7badc9c62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765755"
---
# <a name="iupdateservicecollection-properties"></a>Propriedades de IUpdateServiceCollection

A interface [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection) define as propriedades a seguir.



| Propriedade                                               | Descrição                                                                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get__newenum) | Obtém uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que é usada para enumerar a coleção. |
| [**Contar**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_count)        | Obtém o número de elementos na coleção.                                                                       |
| [**Item**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_item)          | Obtém e define uma interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) na coleção.                               |



 

 

 
