---
description: A interface IUpdateInstallationResult define as propriedades a seguir.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propriedades de IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7574d6fd84afc737d67147c8b40e1e501857f6c19d69bcce4b4b7216bb9c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994406"
---
# <a name="iupdateinstallationresult-properties"></a>Propriedades de IUpdateInstallationResult

A interface [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) define as propriedades a seguir.



| Propriedade                                                           | Descrição                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Obtém **o valor de exceção HRESULT** gerado durante a operação em uma atualização.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Obtém um valor booliana que indica se uma reinicialização do sistema é necessária em um computador para concluir a instalação de uma atualização. |
| [**Resultcode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Obtém [**um valor OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização.          |



 

 

 



