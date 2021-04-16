---
description: 'Saiba mais sobre: níveis de rastreamento do Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Níveis de rastreamento do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761577"
---
# <a name="winsock-tracing-levels"></a>Níveis de rastreamento do Winsock

## <a name="levels-of-winsock-tracing"></a>Níveis de rastreamento de Winsock

Há dois níveis de registro em log possíveis no rastreamento de Winsock:

-   Informações do
-   Detalhado

O nível de informação rastreia eventos de criação e fechamento de soquete, bem como quaisquer erros que ocorram no soquete.

O nível detalhado inclui os eventos de nível de informação e adiciona rastreamento adicional para eventos de envio e recebimento. O log detalhado seria usado para detectar problemas de corrupção de buffer, bem como aplicativos mal escritos.

O nível de informações ou de detalhe pode ser usado com o rastreamento de eventos de rede do Winsock. O rastreamento de alterações do catálogo Winsock dá suporte apenas ao nível de informações.

## <a name="information-event-tracing"></a>Rastreamento de eventos de informações

A lista a seguir fornece detalhes sobre as operações do soquete de evento de rede do Winsock que são rastreadas no nível de informação:

-   Criação de soquete

    Um evento é registrado na criação de soquete, que pode ser usada para rastrear o tempo de vida de um soquete. Esses eventos também incluem soquetes criados por meio da aceitação de conexões em um soquete de escuta.

-   Associar

    O endereço IP local é registrado para ajudar a correlacionar as informações de rastreamento do Winsock às chamadas de soquete de um aplicativo.

-   Conectar

    O endereço IP remoto do Soquete conectado é registrado para ajudar a correlacionar as informações de rastreamento do Winsock às chamadas de soquete de um aplicativo.

-   Anulações e cancelamentos iniciados pelo Winsock

    Sempre que o Winsock aborta ou cancela ativamente uma solicitação, o evento é registrado.

-   Redefinições iniciadas pelo transporte

    Sempre que o transporte subjacente indicar que uma conexão foi redefinida, o evento será registrado.

-   Enviar e receber erros

    Sempre que uma chamada de envio ou recebimento para o transporte subjacente falhar, o evento será registrado.

-   Desconexão e fechamento de soquete

    Um evento é registrado quando um identificador de soquete é fechado.

## <a name="verbose-event-tracing"></a>Rastreamento de eventos detalhado

Todos os eventos de informação são rastreados no nível detalhado. A lista a seguir fornece detalhes sobre as operações adicionais do soquete de evento de rede do Winsock que são rastreadas no nível detalhado:

-   Buffers de envio e recebimento

    Os eventos são registrados em log de endereços de buffer de usuário e comprimentos quando as chamadas de envio e recebimento são postadas no Winsock, bem como na conclusão dessas chamadas. Isso é útil para diagnosticar problemas de reutilização de buffer, bem como o uso ineficiente de buffers.

-   Opções de soquete

    Um evento é registrado quando um aplicativo altera determinados valores de opção de soquete. Algumas das opções registradas incluem \_ SNDBUF, portanto, \_ RCVBUF, SiO \_ habilitam o \_ \_ enfileiramento circular e FIONBIO.

-   WSAPoll e selecione

    Um evento é registrado no uso de um aplicativo de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e [**seleciona**](/windows/desktop/api/Winsock2/nf-winsock2-select) chamadas que podem ser usadas para encontrar afunilamentos de desempenho.

-   Anulações e cancelamentos iniciados pelo Winsock

    Sempre que o Winsock aborta ou cancela ativamente uma solicitação, o evento é registrado.

-   Máscara de evento

    Um evento é registrado na máscara de evento que um aplicativo registra para usar a função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

-   Datagrama

    Um evento é registrado sempre que um datagrama chega e não há espaço de buffer para copiá-lo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Detalhes de rastreamento de eventos de rede do Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
