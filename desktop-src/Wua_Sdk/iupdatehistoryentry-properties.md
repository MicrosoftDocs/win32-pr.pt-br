---
description: A interface IUpdateHistoryEntry define as propriedades a seguir.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Propriedades de IUpdateHistoryEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3acdc9ed32c35028a253944d434c23231c5b6d
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2021
ms.locfileid: "105790370"
---
# <a name="iupdatehistoryentry-properties"></a>Propriedades de IUpdateHistoryEntry

A interface [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) define as propriedades a seguir.



| Propriedade                                                               | Descrição                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Obtém o identificador do aplicativo cliente que processou uma atualização.                                                  |
| [**Data**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Obtém a data e a hora em que uma atualização foi aplicada.                                                                        |
| [**Descrição**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Obtém a descrição de uma atualização.                                                                                       |
| [**Resultado**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Obtém o valor **HRESULT** que é retornado da operação em uma atualização.                                             |
| [**Operacional**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Obtém um valor de [**houver**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) que especifica a operação em uma atualização.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Obtém um valor de [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Obtém o valor [**Serverselection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica qual servidor forneceu uma atualização.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Obtém o identificador de serviço de um serviço de atualização que não é um Windows Update.                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Obtém um hiperlink para as informações de suporte específicas a um idioma para uma atualização.                                             |
| [**Título**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Obtém o título de uma atualização.                                                                                             |
| [**UninstallationNotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Obtém as notas de desinstalação de uma atualização.                                                                              |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Obtém a interface [**isastringcollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) que contém as etapas de desinstalação para uma atualização.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Obtém o código de resultado não mapeado que é retornado de uma operação em uma atualização.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Obtém uma cadeia de caracteres. A cadeia de caracteres contém o identificador exclusivo de uma atualização.                                                   |



 

 

 
