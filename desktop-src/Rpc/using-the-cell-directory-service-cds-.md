---
title: Usando o CDS (serviço de diretório de células)
description: Se você tiver CDS, poderá usá-lo em vez do Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando o serviço de diretório de célula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635929"
---
# <a name="using-the-cell-directory-service-cds"></a>Usando o CDS (serviço de diretório de células)

Se você tiver CDS, poderá usá-lo em vez do Microsoft Locator. Altere as entradas do registro, conforme mostrado:

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

A alteração dessas entradas apontará para um computador de gateway que esteja executando o NSID. Isso será usado como o localizador mestre. No caso de uma falha, não haverá nenhuma pesquisa por uma substituição.

 

 




