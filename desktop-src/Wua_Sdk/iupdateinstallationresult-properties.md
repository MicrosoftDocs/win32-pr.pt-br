---
description: A interface IUpdateInstallationResult define as propriedades a seguir.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propriedades de IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164607"
---
# <a name="iupdateinstallationresult-properties"></a>Propriedades de IUpdateInstallationResult

A interface [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) define as propriedades a seguir.



| Propriedade                                                           | Descrição                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Resultado**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Obtém o valor de exceção **HRESULT** que é gerado durante a operação em uma atualização.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Obtém um valor booliano que indica se uma reinicialização do sistema é necessária em um computador para concluir a instalação de uma atualização. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Obtém um valor de [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização.          |



 

 

 



