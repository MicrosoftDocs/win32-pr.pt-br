---
title: Vários registros de interceptação
description: Várias opções estão disponíveis quando um aplicativo WinSNMP registra uma sessão WinSNMP para interceptações ou notificações.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2149e4ac1e9880601ae64718cd78991718d54a6228488a03e593376d9a7937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009321"
---
# <a name="multiple-trap-registrations"></a>Vários registros de interceptação

Várias opções estão disponíveis quando um aplicativo WinSNMP registra uma sessão WinSNMP para interceptações ou notificações. Por isso, um aplicativo pode chamar a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) várias vezes, em vigor definindo um filtro personalizado para a recepção de interceptações e notificações. Por exemplo, você pode se registrar para um tipo de interceptação ou notificação, ou para todas as interceptações e notificações, dependendo do valor do parâmetro de *notificação* . Além disso, o aplicativo pode especificar valores em outros parâmetros para a função **SnmpRegister** para definir ainda mais as interceptações e as notificações que devem alcançar um aplicativo. Para obter mais informações, consulte [Gerenciando interceptações e notificações](managing-traps-and-notifications.md).

Veja a seguir as instâncias nas quais várias chamadas para **SnmpRegister** são redundantes. Nessas instâncias, **SnmpRegister** retornará snmpapi \_ Success se a função for concluída com êxito, mas o registro redundante é ineficaz.

1.  Uma chamada para a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) solicitando a entrega filtrada de interceptações e notificações para a sessão, após uma chamada anterior para **SnmpRegister** solicitando a entrega de todas as interceptações e notificações (entrega não filtrada). Essa chamada é redundante porque a sessão já está recebendo todas as interceptações e notificações, incluindo o tipo único definido pelo filtro.
2.  Uma chamada duplicada para **SnmpRegister**, ou uma na qual a lista de parâmetros é idêntica à lista de parâmetros em uma chamada anterior a **SnmpRegister** para a sessão.
3.  Uma chamada para a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) solicitando a entrega filtrada de interceptações e notificações com base em um OID (identificador de objeto) cujo prefixo é um OID especificado em uma chamada anterior para **SnmpRegister**. Por exemplo, você pode especificar "1.3.6.1.4.1.311" no parâmetro de *notificação* para receber notificações provenientes de qualquer entidade de agente SNMP da Microsoft. Se você chamar **SnmpRegister** novamente e especificar "1.3.6.1.4.1.311.1", a segunda chamada será redundante porque a sessão já está recebendo todas as interceptações e notificações que contêm o prefixo de OID "1.3.6.1.4.1.311".

Para cancelar o registro da sessão, você deve corresponder a cada chamada de registro exclusiva para a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) . Chame **SnmpRegister** para cancelar o registro da sessão e verifique se os cinco primeiros parâmetros para **SnmpRegister** são idênticos aos da chamada de registro inicial. A única diferença entre a chamada inicial e a chamada de cancelamento de registro é que, ao se registrar, você deve especificar o valor SNMPAPI \_ on no parâmetro *status* e, quando chamar a função para cancelar o registro, deverá especificar snmpapi \_ off. Você não precisa fazer a correspondência de chamadas de registro redundantes para a função **SnmpRegister** . Você só precisa corresponder à primeira chamada de registro exclusiva.

Para alterar os critérios de filtragem, pode ser necessário que um aplicativo primeiro cancele o registro e desabilite a entrega de determinadas interceptações ou notificações. Em seguida, o aplicativo pode criar um novo filtro chamando [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), passando os valores apropriados.

 

 




