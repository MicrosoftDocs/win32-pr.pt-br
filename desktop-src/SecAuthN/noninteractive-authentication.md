---
description: A autenticação não interativa só pode ser usada após a tomada de uma autenticação interativa. Durante a autenticação não interativa, o usuário não insere dados de logon, em vez disso, as credenciais estabelecidas anteriormente são usadas.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Autenticação não interativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658cba212403da2f970e056d7bacc1bc1bcaa559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920853"
---
# <a name="noninteractive-authentication"></a>Autenticação não interativa

A autenticação não interativa só pode ser usada após a tomada de uma [autenticação interativa](interactive-authentication.md) . Durante a autenticação não interativa, o usuário não insere [*dados de logon*](../secgloss/l-gly.md), em vez disso, [*as credenciais*](../secgloss/c-gly.md) estabelecidas anteriormente são usadas.

A autenticação não interativa é executada quando um aplicativo usa a [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) e um pacote de segurança para estabelecer uma conexão de rede segura. A autenticação não interativa é o mecanismo no trabalho quando um usuário se conecta a vários computadores em uma rede sem precisar inserir novamente as informações de logon para cada computador. Por exemplo, se um aplicativo precisar abrir uma pasta segura em um computador remoto e o usuário do aplicativo já estiver conectado interativamente a uma conta de domínio, o aplicativo não exigirá que o usuário forneça dados de logon novamente. Em vez disso, o aplicativo pode solicitar uma autenticação não interativa usando SSPI para passar as informações de segurança estabelecidas anteriormente para um pacote de segurança. O pacote de segurança usa as funções de LSA para verificar as [*credenciais*](../secgloss/c-gly.md). O diagrama a seguir ilustra esse procedimento.

![autenticação não interativa](images/lsasspi2.png)

No diagrama anterior, o aplicativo cliente inicia uma chamada para SSPI para solicitar uma conexão de rede autenticada. O SSPI passa a solicitação do cliente para um pacote de segurança para processamento. O pacote de segurança autentica o usuário chamando a [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) e especificando um [*pacote de autenticação*](../secgloss/a-gly.md) e fornecendo as credenciais existentes do usuário.

O resultado da autenticação é passado do [*pacote de autenticação*](../secgloss/a-gly.md), por meio do LSA, para o [*pacote de segurança*](../secgloss/s-gly.md)e, por fim, para SSPI. O SSPI notifica o aplicativo cliente sobre o resultado da solicitação.

Para obter mais informações sobre o SSPI, consulte [interface do provedor de suporte de segurança](sspi.md).

 

 
