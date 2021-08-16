---
description: A autenticação não interativa só poderá ser usada depois que uma autenticação interativa tiver sido realizada. Durante a autenticação não interativa, o usuário não institui dados de logon; em vez disso, as credenciais estabelecidas anteriormente são usadas.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Autenticação não interativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e259a2b14d48f4d7109966fa01f6fbd6a505a1343e90ea312c557ebfb9c84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786605"
---
# <a name="noninteractive-authentication"></a>Autenticação não interativa

A autenticação não interativa só poderá ser usada depois que [uma autenticação interativa](interactive-authentication.md) tiver sido realizada. Durante a autenticação não interativa, o usuário não institui dados [*de logon,*](../secgloss/l-gly.md)em vez disso, as credenciais [*estabelecidas anteriormente são usadas.*](../secgloss/c-gly.md)

A autenticação não interativa é executada quando um aplicativo usa a [*SSPI (Interface*](../secgloss/s-gly.md) do Provedor de Suporte de Segurança) e um pacote de segurança para estabelecer uma conexão de rede segura. A autenticação não interativa é o mecanismo em ação quando um usuário se conecta a vários máquinas em uma rede sem precisar inserir informações de logon para cada computador. Por exemplo, se um aplicativo precisar abrir uma pasta segura em um computador remoto e o usuário do aplicativo já estiver conectado interativamente a uma conta de domínio, o aplicativo não exigirá que o usuário forneça dados de logon novamente. Em vez disso, o aplicativo pode solicitar uma autenticação não interativa usando o SSPI para passar as informações de segurança estabelecidas anteriormente para um pacote de segurança. Em seguida, o pacote de segurança usa funções LSA para verificar [*as credenciais*](../secgloss/c-gly.md). O diagrama a seguir ilustra este procedimento.

![autenticação não interativa](images/lsasspi2.png)

No diagrama anterior, o aplicativo cliente inicia uma chamada ao SSPI para solicitar uma conexão de rede autenticada. O SSPI passa a solicitação do cliente para um pacote de segurança para processamento. O pacote de segurança autentica o usuário chamando [*a*](../secgloss/a-gly.md) LSA (Autoridade de Segurança [*Local)*](../secgloss/l-gly.md) e especificando um pacote de autenticação e fornecendo as credenciais existentes do usuário.

O resultado da autenticação é passado do [*pacote*](../secgloss/a-gly.md)de [](../secgloss/s-gly.md)autenticação , por meio do LSA, para o pacote de segurança e, por fim, para o SSPI. O SSPI notifica o aplicativo cliente sobre o resultado da solicitação.

Para obter mais informações sobre o SSPI, consulte [Interface do provedor de suporte de segurança](sspi.md).

 

 
