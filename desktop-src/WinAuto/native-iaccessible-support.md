---
title: Suporte nativo do IAccessible
description: Oleacc.dll implementa IAccIdentity em nome de OBJID \_ CLIENT \ 160;ponteiros de interface IAccessible e seus filhos de elemento simples imediatos.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad499b96c668349cc481efd388a780ba094eff2ef6eb4ae52ab041aabea70fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565041"
---
# <a name="native-iaccessible-support"></a>Suporte nativo do IAccessible

Oleacc.dll implementa [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) em nome de ponteiros de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do [**CLIENTE OBJID \_**](object-identifiers.md) e seus filhos de elemento simples imediatos. Um ponteiro de interface **OBJID \_ CLIENT** **IAccessible** é retornado quando [**WM \_ GETOBJECT**](wm-getobject.md) com *lParam*  =  **OBJID \_ CLIENT** é enviado para um **HWND**, que representa a área do cliente da janela ou o controle como um todo. O pai de um ponteiro de interface **IAccessible** normalmente terá uma função de [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) e será o objeto **IAccessible** retornado quando **WM \_ GETOBJECT** com *lParam*  =  [**OBJID \_ WINDOW**](object-identifiers.md) for enviado para um hwnd.

Esses ponteiros de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) normalmente ocorrem em que um proxy do Oleacc.dll é subclasse ou em que um controle personalizado simples (como um **contêiner IAccessible** mais um nível de filhos de elemento simples) fornece uma implementação **IAccessible** nativa.

Implementações [**de IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativas mais complicadas, como onde existe uma hierarquia de **IAccessible** s ou onde as IDs de objeto personalizadas são usadas devem implementar [**iAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) em si.

 

 




