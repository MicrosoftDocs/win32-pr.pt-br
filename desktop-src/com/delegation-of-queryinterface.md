---
title: Delegação de QueryInterface
description: Delegação de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c63a9eb336bcf049877957bd55523ee70de489263bd19e0ebece8b65fbdd0ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501206"
---
# <a name="delegation-of-queryinterface"></a>Delegação de QueryInterface

Manipuladores que exigem acesso a algumas das interfaces internas no gerenciador de proxy precisam passar pela interface [**IInternalUnknown.**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) Isso impede que os manipuladores delegarem e expondo às escuras as interfaces internas do agregado fora da agregação. Essas interfaces incluem [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI.**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) Se o manipulador quiser expor **IClientSecurity** ou **IMultiQI,** ele deverá implementá-los em si.

No caso de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), se o cliente tentar definir a segurança em uma interface que o manipulador expôs, o manipulador deverá definir a segurança no proxy de interface de rede subjacente.

No caso do [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), o manipulador deve preencher as interfaces que ele conhece e, em seguida, encaminhar a chamada para o gerenciador de proxy para obter o restante das interfaces preenchidas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador de Client-Side lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 