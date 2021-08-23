---
description: A interface IUpdateServiceCollection define as propriedades a seguir.
ms.assetid: 340a63ee-8e31-467d-88d2-f320ccc0f054
title: Propriedades de IUpdateServiceCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63a99d15f95c086bb8c1b062e76015f00d8214f64e5b4f73ed2832f1f5fab99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814999"
---
# <a name="iupdateservicecollection-properties"></a>Propriedades de IUpdateServiceCollection

A interface [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection) define as propriedades a seguir.



| Propriedade                                               | Descrição                                                                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get__newenum) | Obtém uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que é usada para enumerar a coleção. |
| [**Contagem**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_count)        | Obtém o número de elementos na coleção.                                                                       |
| [**Item**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_item)          | Obtém e define uma interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) na coleção.                               |



 

 

 
