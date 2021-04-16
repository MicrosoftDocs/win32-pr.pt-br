---
description: Requisitos de Server-Side para representação
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Requisitos de Server-Side para representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765145"
---
# <a name="server-side-requirements-for-impersonation"></a>Requisitos de Server-Side para representação

O servidor executa a representação programaticamente. Ele assume explicitamente as credenciais de segurança do cliente usando [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). Quando o cliente tiver concedido a autoridade suficiente do servidor, isso terá o efeito de substituir as credenciais de segurança do cliente pelo token de thread do servidor, no lugar do token do processo.

Quando isso tiver sido feito, o servidor poderá, por exemplo, usar o token do cliente para acessar recursos protegidos com um descritor de segurança. Ou pode fazer chamadas sob a identidade do cliente, se o encobrimento estiver habilitado.

O servidor pode definir explicitamente o encobrimento programaticamente ou pode contar com uma configuração administrativa. Por padrão, os aplicativos COM+ são configurados para usar o encobrimento dinâmico. Para obter mais detalhes, consulte [encobrindo](cloaking.md).

Se o servidor estiver implementando a delegação em nome do cliente — usando a identidade do cliente pela rede — a identidade do processo do servidor deverá ser marcada como "confiável para delegação" no serviço de Active Directory; caso contrário, haverá falha na delegação.

Quando terminar de usar a identidade do cliente, o servidor poderá reverter para seu próprio token de processo usando o [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).

Para obter detalhes sobre como implementar a representação e a delegação, consulte [delegação e representação](/windows/desktop/com/delegation-and-impersonation).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos do lado do cliente para representação](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Encobrimento](cloaking.md)
</dt> </dl>

 

 
