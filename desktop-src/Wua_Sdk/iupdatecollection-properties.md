---
description: A interface IUpdateCollection define as propriedades a seguir.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propriedades de IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761508"
---
# <a name="iupdatecollection-properties"></a>Propriedades de IUpdateCollection

A interface [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) define as propriedades a seguir.



| Propriedade                                        | Descrição                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Obtém uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que pode ser usada para enumerar a coleção. |
| [**Contar**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Obtém o número de elementos na coleção.                                                                           |
| [**Item**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Obtém ou define uma interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) em uma coleção.                                                    |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Obtém um valor booliano que indica se a coleção de atualizações é somente leitura.                                          |



 

 

 
