---
description: Requisitos de Client-Side para representação
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Requisitos de Client-Side para representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296131"
---
# <a name="client-side-requirements-for-impersonation"></a>Requisitos de Client-Side para representação

As duas configurações a seguir podem ser especificadas em relação à representação no lado do cliente:

-   Nível de representação, que indica a disposição do cliente para fazer com que o servidor use sua identidade.
-   Uma configuração no serviço de Active Directory por meio do qual a conta do cliente pode ser marcada como "a conta é confidencial e não pode ser delegada", o que desabilitará a delegação.

O nível de representação pode ser definido de várias maneiras. Se o cliente não indicar um nível de representação, o padrão em todo o computador será usado pelo COM. O padrão em todo o computador pode ser definido usando a ferramenta administrativa serviços de componentes ou Dcomcnfg.exe. O cliente também pode indicar um nível de representação preferencial administrativamente com Dcomcnfg.exe.

O cliente pode indicar o nível de representação programaticamente, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)— equivalente a [**IClientSecurity:: setampla**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), que pode ser chamado sempre que necessário — ou [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que pode ser chamado uma vez por processo.

Se o cliente indicar representação de nível delegado — a autoridade mais ampla que ele pode conceder ao servidor — o cliente deve estar sendo executado sob uma identidade configurada corretamente no serviço de Active Directory para permitir que sua identidade seja delegada.

Para obter mais detalhes sobre os níveis de representação e os requisitos para a delegação funcionar, consulte [delegação e representação](/windows/desktop/com/delegation-and-impersonation).

Os aplicativos COM+ sempre podem atuar como clientes, é claro. Quando o aplicativo COM+ faz uma chamada para outro aplicativo ou recurso, ele expressa um nível de representação. Para aplicativos de servidor do COM+, você pode definir um nível de representação administrativamente. Os aplicativos de biblioteca COM+ não podem definir seu próprio nível de representação; em vez disso, eles usam o processo de host. Para saber como definir a representação para um aplicativo COM+, consulte [definindo um nível de representação](setting-an-impersonation-level.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Encobrimento](cloaking.md)
</dt> <dt>

[Requisitos do lado do servidor para representação](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
