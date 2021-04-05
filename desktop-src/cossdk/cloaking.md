---
description: Há dois ingredientes para determinar o comportamento da representação da autoridade que o cliente concede explicitamente ao servidor por meio de um nível de representação e a capacidade dos servidores de mascarar sua própria identidade ao fazer chamadas nos clientes.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Encobrimento (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646295"
---
# <a name="cloaking-component-services"></a>Encobrimento (serviços de componentes)

Há dois ingredientes para determinar o comportamento da representação: a autoridade que o cliente concede explicitamente ao servidor por meio de um nível de representação e a capacidade do servidor de mascarar sua própria identidade ao fazer chamadas em nome do cliente. Essa última funcionalidade é conhecida como *encobrindo*. O encobrimento tem a ver com a identidade de segurança sob a qual o servidor faz chamadas.

Quando o servidor representa o cliente, ele tem acesso direto às credenciais de segurança do cliente. Em um sentido muito local, o thread do servidor assume a identidade do cliente. Mas quando o servidor faz chamadas fora de seu processo, a identidade do cliente não será necessariamente projetada como a identidade sob a qual a chamada é feita.

Quando o encobrimento está habilitado, as chamadas feitas pelo servidor representando o cliente podem ser feitas sob a identidade do cliente. Quando o encobrimento estiver desabilitado, as chamadas pelo servidor serão feitas sob a identidade do servidor.

Além disso, há duas formas de encobrimento, encobrimento *estático* e *encobrimento dinâmico*, que podem ser descritas da seguinte maneira:

-   Representação com encobrimento estático. A identidade do cliente original (realizada como o token de thread do servidor) pode ser apresentada uma vez a um servidor downstream em uma chamada usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), definindo a identidade do cliente original uma vez no proxy e esse token de thread será usado em chamadas de método subsequentes.
-   Representação com o encobrimento dinâmico. A identidade original do cliente é descoberta como o token de thread do servidor em cada chamada de método para o servidor downstream. Na verdade, a identidade apresentada pode ser determinada dinamicamente. A sobrecarga necessária para fazer isso pode ser consideravelmente mais cara.

Para aplicativos COM+, a configuração padrão é para o recurso de encobrimento dinâmico. Isso pode ser alterado programaticamente e administrativamente. Embora o encobrimento dinâmico possa ter sobrecarga de desempenho, ele fornece a flexibilidade que geralmente é exigida pelas circunstâncias que exigem o uso da representação em primeiro lugar.

Para obter mais detalhes sobre o encobrimento e descrições precisas de possíveis comportamentos, consulte [encobrindo](/windows/desktop/com/cloaking) na documentação com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos do lado do cliente para representação](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Requisitos do lado do servidor para representação](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
