---
title: Funções da API do WebDAV
description: As funções a seguir são usadas na API do WebDAV.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401f527bcd98f86f8116df5b25ba1ea71e0f432e19dc89eae00582a2a0b4865e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995036"
---
# <a name="webdav-api-functions"></a>Funções da API do WebDAV

As funções a seguir são usadas na API do WebDAV.



| Função                                                             | Descrição                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Cria uma conexão segura com um servidor WebDAV ou um arquivo ou diretório remoto em um servidor WebDAV.                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | O cliente WebDAV chama a função de retorno de chamada [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) definida pelo aplicativo para solicitar as credenciais ao usuário.                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Fecha todas as conexões com um servidor WebDAV ou um arquivo ou diretório remoto em um servidor WebDAV.                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Fecha uma conexão que foi criada usando a função [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) .                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Libera os dados da versão local de um arquivo remoto para o servidor WebDAV.                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | O cliente WebDAV chama a função de retorno de chamada [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) definida pelo aplicativo para liberar as informações de credencial que foram recuperadas pela função de retorno de chamada [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) . |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Recupera as informações do código de erro estendido que o servidor WebDAV retornou para a operação de e/s com falha anterior.                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Converte o caminho UNC especificado em um caminho HTTP equivalente.                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Retorna o proprietário do bloqueio de arquivo para um arquivo que está bloqueado em um servidor WebDAV.                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Converte o caminho HTTP especificado em um caminho UNC equivalente.                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Invalida o conteúdo do cache local para um arquivo remoto em um servidor WebDAV.                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Registra uma função de retorno de chamada definida pelo aplicativo que o cliente WebDAV pode usar para solicitar as credenciais ao usuário.                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Cancela o registro de uma função de retorno de chamada registrada que o cliente WebDAV usa para solicitar as credenciais ao usuário.                                                                                                                            |



 

 

 




