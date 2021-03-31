---
title: Gerenciando a política de retransmissão
description: O aplicativo WinSNMP pode solicitar que a implementação do Microsoft WinSNMP execute a política de retransmissão do aplicativo. Quando a implementação gerencia a retransmissão, ela usa o período de tempo limite e os valores de contagem de repetição em seu banco de dados.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005848"
---
# <a name="managing-the-retransmission-policy"></a>Gerenciando a política de retransmissão

O aplicativo WinSNMP pode solicitar que a implementação do Microsoft WinSNMP execute a política de retransmissão do aplicativo. Quando a implementação gerencia a retransmissão, ela usa o período de tempo limite e os valores de contagem de repetição em seu banco de dados.

A implementação identifica o modo de retransmissão padrão em um valor de retorno da função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante a inicialização. O modo pode ser um dos valores a seguir.



| Valor        | Significado                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_ em  | A implementação está executando a política de retransmissão do aplicativo.     |
| SNMPAPI \_ desativado | A implementação não está executando a política de retransmissão do aplicativo. |



 

Um aplicativo WinSNMP pode recuperar a qualquer momento o modo de retransmissão atual em vigor para a implementação chamando a função [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) . A API WinSNMP fornece outras [funções de banco de dados](winsnmp-functions.md) que simplificam o gerenciamento da política de retransmissão.

A qualquer momento durante a execução do programa, o aplicativo WinSNMP pode ajustar a execução da política executando uma das seguintes etapas:

-   Solicite que a implementação inicie ou pare de executar a política de retransmissão chamando a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . Para obter mais informações, consulte [ativando e](turning-retransmission-on-and-off.md)desativando a retransmissão.
-   Modifique o período de tempo limite e repita a contagem de valores no banco de dados da implementação. Para obter mais informações, consulte [alterando a política de retransmissão](changing-the-retransmission-policy.md).
-   Chame a função [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) para cancelar o ciclo de retransmissão e liberar estruturas de dados internas associadas a uma única solicitação de mensagem SNMP. Para obter mais informações, consulte [cancelando a retransmissão](canceling-retransmission.md).

O aplicativo pode executar sua própria política de retransmissão. Nesse caso, a execução pode ou não ser baseada nos valores no banco de dados.

 

 




