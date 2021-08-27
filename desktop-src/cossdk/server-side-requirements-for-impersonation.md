---
description: Server-Side requisitos de representação
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side requisitos de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e43016428f2ff083fc5a783d05c3c79e241dcf299f3af9ca226cb4f6a2cf1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096796"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side requisitos de representação

O servidor executa a representação programaticamente. Ele assume explicitamente as credenciais de segurança do cliente usando [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). Quando o cliente concedeu ao servidor autoridade suficiente, isso tem o efeito de substituir as credenciais de segurança do cliente pelo token de thread do servidor, no lugar do token de processo.

Quando isso for feito, o servidor poderá, por exemplo, usar o token do cliente para acessar recursos protegidos com um descritor de segurança. Ou pode fazer chamadas na identidade do cliente, se a reação estiver habilitada.

O servidor pode definir explicitamente a desajuste programaticamente ou pode depender de uma configuração administrativa. Por padrão, os aplicativos COM+ são configurados para usar a replicação dinâmica. Para obter mais detalhes, consulte [Detalhando](cloaking.md).

Se o servidor estiver implementando a delegação em nome do cliente , usando a identidade do cliente pela rede, a identidade do processo do servidor deverá ser marcada como "Confiável para delegação" no Serviço do Active Directory; caso contrário, a delegação falhará.

Quando terminar de usar a identidade do cliente, o servidor poderá reverter para seu próprio token de processo usando [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).

Para obter detalhes sobre como implementar a representação e a delegação, consulte [Delegação e representação.](/windows/desktop/com/delegation-and-impersonation)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação do cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos do lado do cliente para representação](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Camuflagem](cloaking.md)
</dt> </dl>

 

 
