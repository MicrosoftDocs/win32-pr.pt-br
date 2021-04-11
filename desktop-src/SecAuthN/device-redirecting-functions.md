---
description: As funções de redirecionamento de dispositivo redirecionam dispositivos MS-DOS padrão, letras de unidade e portas LPT. Isso permite que os aplicativos em execução no sistema usem os dispositivos e acessem a rede de uma maneira totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Funções de Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164287"
---
# <a name="device-redirecting-functions"></a>Funções de Device-Redirecting

As funções de redirecionamento de dispositivo redirecionam dispositivos MS-DOS padrão, letras de unidade e portas LPT. Isso permite que os aplicativos em execução no sistema usem os dispositivos e acessem a rede de uma maneira totalmente transparente.



| Função                                                         | Descrição                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Redireciona ou conecta um dispositivo local a um recurso de rede.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Executa a mesma ação que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), mas permite que o usuário especifique qual janela deve ter qualquer caixa de diálogo e como a conexão deve ser estabelecida.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrompe uma conexão de rede. As alterações serão lembradas se um dispositivo for desconectado, a menos que a conexão seja uma conexão sem dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Retorna informações sobre uma conexão.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Retorna informações sobre uma conexão, mesmo se a conexão estiver desconectada no momento.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Retorna informações de desempenho sobre uma conexão.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Retorna o nome universal ou local remoto, no formato especificado durante a chamada de função.<br/>                                                                                            |



 

 

 




