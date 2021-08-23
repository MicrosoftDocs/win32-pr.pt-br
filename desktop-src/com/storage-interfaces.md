---
title: Armazenamento Interfaces
description: Armazenamento Interfaces
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c378b37c020f15e0fe497249b2834faffefc232bc184564f80fdb247550033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129698"
---
# <a name="storage-interfaces"></a>Armazenamento Interfaces

Os contêineres de controle devem ser capazes de dar suporte a controles que implementam [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Opcionalmente, um contêiner pode dar suporte a qualquer outra interface de persistência, como [**IPersistMemory,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para os controles que oferecem suporte.

Depois que um contêiner de controle ActiveX tiver escolhido e inicializado uma interface de armazenamento a ser usada ([**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)etc),essa interface de armazenamento permanecerá a interface de armazenamento primária durante o tempo de vida do controle, ou seja, o controle permanecerá em posse do armazenamento. Isso não impede que o contêiner seja salvo em outras interfaces de armazenamento.

ActiveX contêineres de controle não precisam dar suporte a um mecanismo salvar como texto, portanto, usar [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) e a interface do lado do contêiner [**associada IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) são opcionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 