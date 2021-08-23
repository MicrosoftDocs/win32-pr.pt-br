---
description: As funções de redirecionamento de dispositivo redirecionam dispositivos MS-DOS padrão, letras de unidade e portas LPT. Isso permite que os aplicativos em execução no sistema usem os dispositivos e acessem a rede de maneira totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4929052ed2691d6264791cac431e59faaacdb92f7f96bb610d99fdd4ded471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008444"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting funções

As funções de redirecionamento de dispositivo redirecionam dispositivos MS-DOS padrão, letras de unidade e portas LPT. Isso permite que os aplicativos em execução no sistema usem os dispositivos e acessem a rede de maneira totalmente transparente.



| Função                                                         | Descrição                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Redireciona ou conecta um dispositivo local a um recurso de rede.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Executa a mesma ação que [**NPAddConnection,**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)mas permite que o usuário especifique qual janela deve ter as caixas de diálogo e como a conexão deve ser estabelecida.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrompe uma conexão de rede. As alterações serão lembradas se um dispositivo estiver desconectado, a menos que a conexão seja uma conexão sem dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Retorna informações sobre uma conexão.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Retorna informações sobre uma conexão, mesmo se a conexão estiver desconectada no momento.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Retorna informações de desempenho sobre uma conexão.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Retorna o nome universal remoto ou local, no formato especificado durante a chamada de função.<br/>                                                                                            |



 

 

 




