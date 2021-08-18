---
title: Usando o CDS (Serviço de Diretório de Célula)
description: Se você tiver CDS, poderá usá-lo em vez do Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, usando o serviço de diretório de célula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010632"
---
# <a name="using-the-cell-directory-service-cds"></a>Usando o CDS (Serviço de Diretório de Célula)

Se você tiver CDS, poderá usá-lo em vez do Microsoft Locator. Altere as entradas do Registro conforme mostrado:

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

Alterar essas entradas apontará para um computador gateway que está executando o NSID. Isso será usado como o localizador mestre. No caso de uma falha, não haverá nenhuma pesquisa para uma substituição.

 

 




