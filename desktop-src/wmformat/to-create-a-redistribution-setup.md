---
title: Para criar uma configuração de redistribuição
description: Para criar uma configuração de redistribuição
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows SDK de formato de mídia, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- Windows SDK do formato de mídia, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, criando
- redistribuição de software WMFDist.exe
- redistribuição, criando
- redistribuição, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb26b63a2379a72e2d97df876d91d8c57a6da9249c4e40525e81edacaf86542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027294"
---
# <a name="to-create-a-redistribution-setup"></a>Para criar uma configuração de redistribuição

1.  Faça com que sua rotina de instalação instale os arquivos do aplicativo e faça as configurações necessárias antes de invocar o pacote de redistribuição.
2.  Instale o WMFDist.exe. Você pode usar o sinalizador/Q: a para fazer uma instalação silenciosa, autônoma e suprimir a interface do usuário da configuração de redistribuição durante a instalação do seu aplicativo. Sua rotina deve detectar se a reinicialização é necessária no final.

    Por exemplo:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuição de software**](software-redistribution.md)
</dt> </dl>

 

 




