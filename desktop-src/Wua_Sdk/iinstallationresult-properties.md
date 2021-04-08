---
description: A interface IInstallationResult define as propriedades a seguir.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propriedades de IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010550"
---
# <a name="iinstallationresult-properties"></a>Propriedades de IInstallationResult

A interface [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) define as propriedades a seguir.



| Propriedade                                                     | Descrição                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Resultado**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Obtém o **HRESULT** da exceção, se houver, que é gerado durante a instalação.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Obtém um valor booliano que indica se você deve reiniciar o computador para concluir a instalação ou desinstalação de uma atualização. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Obtém um valor de [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização.               |



 

 

 



