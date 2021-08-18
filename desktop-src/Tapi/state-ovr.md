---
description: O estado de sessão ou chamada indica o status atual de uma sessão, como &\# 0034;offering&\# 0034; ou &\# 0034;connected.&\# 0034; O tratamento adequado das informações de estado é vital para o funcionamento adequado da maioria dos aplicativos TAPI.
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: Estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138b9daa01623f2be95c9b620526be9ed55c8384532410ac1f69ed3f2dd97bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862044"
---
# <a name="state"></a>Estado

O estado de sessão ou chamada indica o status atual de uma sessão, como "oferta" ou "conectada". O tratamento adequado das informações de estado é vital para o funcionamento adequado da maioria dos aplicativos TAPI. Por exemplo, a operação de resposta pode ser executada somente em uma sessão oferecida, mas uma transferência falhará se a sessão estiver nesse estado.

O estado de uma sessão muda como resultado de eventos. Os eventos podem ser solicitados ou não solicitados. *Os eventos solicitados* são causados pelo aplicativo que controla a sessão, como quando ele invoca uma operação de sessão TAPI. *Eventos não solicitados* são causados pela opção, pela rede telefônica, pelo usuário pressionando botões no telefone local ou pelas ações da parte remota.

Sempre que um provedor de serviços detecta uma alteração de estado de sessão, ele relata a alteração para TAPI e a TAPI emite uma notificação de evento para todos os aplicativos proprietários e monitorados. O aplicativo deve reagir a essas notificações adequadamente. Consulte Notificação de Eventos em [Inicialização tapi](tapi-initialization.md) para obter informações sobre como controlar quais eventos são relatados a um aplicativo.

Um aplicativo sempre deve processar notificações de eventos de estado. Transições de estado válidas para uma configuração física podem ser inválidas para outra. Por exemplo, considere uma linha que termina fisicamente no computador e em um conjunto de telefone separado, criando uma configuração de linha de parte entre o computador e o conjunto de telefone. Um aplicativo em execução no computador pode não saber sobre atividades do conjunto de telefone. Ou seja, a linha pode estar em uso sem que o provedor de serviços esteja ciente dela. Um aplicativo que tenta fazer uma chamada de saída terá êxito ao alocar uma aparência de chamada da TAPI, mas isso resulta no compartilhamento da chamada ativa na linha. Enviar uma cadeia de caracteres discada DTMF sem primeiro verificar se há um tom de discagem pode não resultar no comportamento pretendido (ou escuro).

Um aplicativo não deve assumir uma progressão rígida de um estado para outro. Os eventos de estado chegam e são encaminhados de forma assíncrona e as notificações podem não ser recebidas em uma ordem previsível. Portanto, as notificações de estado de chamada devem ser exibidas como informando ao aplicativo o novo estado da chamada, em vez de relatar as transições entre dois estados.

Todos os provedores de serviços de telefonia devem fornecer essas informações.

**TAPI 2.x: **[**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**mensagem LINE \_ CALLSTATE,**](./line-callstate.md) [ \_ constantes LINECALLSTATE](./linecallstate--constants.md)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro \_ CALLID CIL** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**notificação ITCallStateEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) [**enumerador CALL \_ STATE**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state)

 

 
