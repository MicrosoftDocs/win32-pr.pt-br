---
description: Estado de sessão ou chamada indica o status atual de uma sessão, como &\# 0034; oferta&\# 0034; ou &\# 0034; conectado. &\# 0034; A manipulação adequada de informações de estado é vital para o funcionamento adequado da maioria dos aplicativos TAPI.
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: Estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fb9c482fcb9e432b5bfb5d36f77cd09f538086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767737"
---
# <a name="state"></a>Estado

Estado de sessão ou chamada indica o status atual de uma sessão, como "oferta" ou "conectado". A manipulação adequada de informações de estado é vital para o funcionamento adequado da maioria dos aplicativos TAPI. Por exemplo, a operação de resposta pode ser executada somente em uma sessão oferecida, mas uma transferência falhará se a sessão estiver nesse estado.

O estado de uma sessão é alterado como resultado de eventos. Os eventos podem ser solicitados ou não solicitados. Os *eventos solicitados* são causados pelo aplicativo que controla a sessão, como quando ele invoca uma operação de sessão TAPI. Os *eventos não solicitados* são causados pela opção, pela rede telefônica, pelo usuário que pressiona os botões no telefone local ou pelas ações da parte remota.

Sempre que um provedor de serviços detecta uma alteração de estado de sessão, ele relata que a alteração para TAPI e TAPI emite uma notificação de eventos para todos os aplicativos de proprietário e monitor. O aplicativo deve reagir a essas notificações adequadamente. Consulte a notificação de eventos sob [inicialização TAPI](tapi-initialization.md) para obter informações sobre como controlar quais eventos são relatados para um aplicativo.

Um aplicativo sempre deve processar notificações de eventos de estado. As transições de estado válidas para uma configuração física podem ser inválidas para outra. Por exemplo, considere uma linha que termina fisicamente no computador e em um conjunto de telefone separado, criando uma configuração de linha de terceiros entre o computador e o conjunto de telefone. Um aplicativo em execução no computador pode não saber sobre as atividades do conjunto de telefone. Ou seja, a linha pode estar em uso sem que o provedor de serviços esteja ciente dela. Um aplicativo que tenta fazer uma chamada de saída terá sucesso em alocar uma aparência de chamada da TAPI, mas isso resulta no compartilhamento da chamada ativa na linha. O envio cego de uma cadeia de caracteres de discagem DTMF sem primeiro verificar um tom de discagem pode não resultar no comportamento pretendido (ou educado).

Um aplicativo não deve assumir uma progressão rígida de um estado para outro. Os eventos de estado chegam e são encaminhados de forma assíncrona e as notificações não podem ser recebidas em uma ordem previsível. Portanto, as notificações de estado de chamada devem ser exibidas como informando ao aplicativo o novo estado de chamada em vez de relatar as transições entre dois Estados.

Todos os provedores de serviços de telefonia devem fornecer essas informações.

* * TAPI 2. x: * *[**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**mensagem \_ Callstate de linha**](./line-callstate.md) , [ \_ constantes LINECALLSTATE](./linecallstate--constants.md)

**TAPI 3. x: **[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro \_ callid cil** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), notificação [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) , enumerador de [**\_ estado de chamada**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state)

 

 
