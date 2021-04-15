---
description: A interface IUpdateService define as propriedades a seguir.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Propriedades de IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461162"
---
# <a name="iupdateservice-properties"></a>Propriedades de IUpdateService

A interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) define as propriedades a seguir.



| Propriedade                                                              | Descrição                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CanRegisterWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | Obtém um valor booliano que indica se o serviço pode ser registrado com Atualizações Automáticas.    |
| [**ContentValidationCert**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | Obtém um hash SHA-1 do certificado que é usado para assinar o conteúdo do serviço.         |
| [**ExpirationDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | Obtém a data em que o arquivo de gabinete de autorização expira.                                  |
| [**IsManaged**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | Obtém um valor booliano que indica se um serviço é um serviço gerenciado.                     |
| [**IsRegisteredWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | Obtém um valor booliano que indica se um serviço está registrado com Atualizações Automáticas.     |
| [**IsScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | Obtém um valor booliano que indica se um serviço é baseado em um pacote de verificação.               |
| [**Emitido**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | Obtém a data em que o arquivo de gabinete de autorização foi emitido.                               |
| [**Nome**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | Obtém o nome do serviço.                                                                   |
| [**OffersWindowsUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | Obtém um valor booliano que indica se o serviço atual oferece atualizações de atualizações do Windows. |
| [**RedirectUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | Obtém a URL para o arquivo de gabinete do redirecionador.                                                   |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | Obtém o identificador de um serviço.                                                              |
| [**ServiceUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | Obtém a URL para o serviço.                                                                   |
| [**SetupPrefix**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | Obtém o prefixo dos arquivos de instalação.                                                            |



 

 

 



