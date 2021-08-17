---
description: A interface IUpdateHistoryEntry define as propriedades a seguir.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Propriedades de IUpdateHistoryEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5c6951857f72f4a9ee4f86cd29d42e024e05b87d58d589043f5a40e951d4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738265"
---
# <a name="iupdatehistoryentry-properties"></a>Propriedades de IUpdateHistoryEntry

A interface [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) define as propriedades a seguir.



| Propriedade                                                               | Descrição                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Obtém o identificador do aplicativo cliente que processou uma atualização.                                                  |
| [**Data**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Obtém a data e a hora em que uma atualização foi aplicada.                                                                        |
| [**Descrição**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Obtém a descrição de uma atualização.                                                                                       |
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Obtém **o valor HRESULT** retornado da operação em uma atualização.                                             |
| [**Operação**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Obtém [**um valor UpdateOperation**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) que especifica a operação em uma atualização.                      |
| [**Resultcode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Obtém [**um valor OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Obtém [**o valor ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica qual servidor forneceu uma atualização.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Obtém o identificador de serviço de um serviço de atualização que não é uma Windows atualização.                                           |
| [**Supporturl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Obtém um hiperlink para as informações de suporte específicas do idioma para uma atualização.                                             |
| [**Título**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Obtém o título de uma atualização.                                                                                             |
| [**DesinstalaçãoNotas**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Obtém as notas de desinstalação de uma atualização.                                                                              |
| [**DesinstalaçãoEtapas**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Obtém a interface [**IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) que contém as etapas de desinstalação para uma atualização.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Obtém o código de resultado não mapeado retornado de uma operação em uma atualização.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Obtém uma cadeia de caracteres. A cadeia de caracteres contém o identificador exclusivo de uma atualização.                                                   |



 

 

 
