---
title: Abrindo e fechando uma sessão WinSNMP
description: Para abrir uma sessão, um aplicativo chama a função SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41871c9adc2f7fcefc04b5816b29685ad6b1516a6238c1855ed41e878d5b2736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009194"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Abrindo e fechando uma sessão WinSNMP

Para abrir uma sessão, um aplicativo chama a função [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) . Se a função for concluída com êxito, a implementação do Microsoft WinSNMP abrirá uma sessão e a função retornará um identificador de sessão na forma de um identificador de **\_ sessão HSNMP** . Todas as funções de WinSNMP que retornam variáveis de identificador incluem o identificador de sessão como um parâmetro de entrada. Isso permite que a implementação use o identificador para gerenciar com eficiência os recursos no nível da sessão.

Um aplicativo pode ter várias sessões abertas ao mesmo tempo. Várias sessões em um aplicativo podem compartilhar variáveis de identificador.

Se a implementação não puder abrir uma sessão devido a limitações de recursos, ela retornará SNMPAPI \_ falha quando o aplicativo chamar [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Se o aplicativo chamar a função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , ele retornará um erro de alocação de snmpapi \_ \_ .

Uma chamada para a função [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permite que a implementação libere todos os recursos restantes e feche a sessão.

Para obter mais informações, consulte [objetos de manipulador de recursos](resource-handle-objects.md) e sessões de [WinSNMP](winsnmp-sessions.md).

 

 




