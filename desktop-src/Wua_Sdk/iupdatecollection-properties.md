---
description: A interface IUpdateCollection define as propriedades a seguir.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propriedades de IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599e7ba6efd20810ad61a8f59f5cfec67ce82b9e95f42df5250360238c43d044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859756"
---
# <a name="iupdatecollection-properties"></a>Propriedades de IUpdateCollection

A interface [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) define as propriedades a seguir.



| Propriedade                                        | Descrição                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Obtém uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que pode ser usada para enumerar a coleção. |
| [**Contagem**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Obtém o número de elementos na coleção.                                                                           |
| [**Item**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Obtém ou define uma interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) em uma coleção.                                                    |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Obtém um valor booliano que indica se a coleção de atualizações é somente leitura.                                          |



 

 

 
