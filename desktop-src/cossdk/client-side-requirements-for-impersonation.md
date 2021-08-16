---
description: Client-Side requisitos de representação
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side requisitos de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb47c2ffb5f3b8e443d2dc50add83a39b5dfc1ee31a6909c34b0170a85db11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308525"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side requisitos de representação

As duas configurações a seguir podem ser especificadas em relação à representação no lado do cliente:

-   Nível de representação, que indica a disposição do cliente de fazer com que o servidor use sua identidade.
-   Uma configuração no Serviço do Active Directory por meio da qual a conta do cliente pode ser marcada como "A conta é sensível e não pode ser delegada", o que desabilitará a delegação.

O nível de representação pode ser definido de várias maneiras. Se o cliente não indicar um nível de representação, o padrão de todo o computador será usado pelo COM. O padrão em todo o computador pode ser definido usando a ferramenta administrativa serviços de componentes ou Dcomcnfg.exe. O cliente também pode indicar um nível de representação preferencial administrativamente com Dcomcnfg.exe.

O cliente pode indicar o nível de representação programaticamente, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)— equivalente a [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), que pode ser chamado sempre que necessário — ou [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que pode ser chamado uma vez por processo.

Se o cliente indicar a representação no nível de delegado , a autoridade mais ampla que ele pode conceder ao servidor, o cliente deverá estar em execução em uma identidade configurada corretamente no Serviço do Active Directory para permitir que sua identidade seja delegada.

Para obter mais detalhes sobre os níveis de representação e os requisitos para a delegação funcionar, consulte [Delegação e representação](/windows/desktop/com/delegation-and-impersonation).

Aplicativos COM+ sempre podem atuar como clientes, é claro. Quando o aplicativo COM+ faz uma chamada para outro aplicativo ou recurso, ele expressa um nível de representação. Para aplicativos de servidor COM+, você pode definir um nível de representação administrativamente. Os aplicativos de biblioteca COM+ não podem definir seu próprio nível de representação; em vez disso, eles usam o do processo de host. Para saber como definir a representação para um aplicativo COM+, consulte [Definindo um nível de representação](setting-an-impersonation-level.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação do cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Camuflagem](cloaking.md)
</dt> <dt>

[Requisitos do lado do servidor para representação](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
