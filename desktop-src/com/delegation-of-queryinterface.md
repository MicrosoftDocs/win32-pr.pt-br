---
title: Delegação de QueryInterface
description: Delegação de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084923"
---
# <a name="delegation-of-queryinterface"></a>Delegação de QueryInterface

Os manipuladores que exigem acesso a algumas interfaces internas no Gerenciador de proxy precisam passar pela interface [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) . Isso impede que os manipuladores delegom e exponham indistintamente as interfaces internas do agregado fora da agregação. Essas interfaces incluem [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi). Se o manipulador quiser expor **IClientSecurity** ou **IMultiQI**, ele deverá implementá-lo por conta própria.

No caso do [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), se o cliente tentar definir a segurança em uma interface que o manipulador tenha exposto, o manipulador deverá definir a segurança no proxy de interface de rede subjacente.

No caso do [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), o manipulador deve preencher as interfaces que ele conhece e, em seguida, encaminhar a chamada para o Gerenciador de proxy para obter o restante das interfaces preenchidas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador de Client-Side leve](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 