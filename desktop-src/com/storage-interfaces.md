---
title: Interfaces de armazenamento
description: Interfaces de armazenamento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549261"
---
# <a name="storage-interfaces"></a>Interfaces de armazenamento

Os contêineres de controle devem ser capazes de dar suporte a controles que implementam [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Opcionalmente, um contêiner pode dar suporte a qualquer outra interface de persistência, como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para esses controles que fornecem suporte.

Depois que um contêiner de controle ActiveX tiver escolhido e inicializado uma interface de armazenamento para usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), essa interface de armazenamento permanecerá na interface de armazenamento primária durante o tempo de vida do controle, ou seja, o controle permanecerá em posse do armazenamento. Isso não impede que o contêiner seja salvo em outras interfaces de armazenamento.

Os contêineres de controle ActiveX não precisam dar suporte a um mecanismo salvar como texto, portanto, usar [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) e a interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) associada do lado do contêiner são opcionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 