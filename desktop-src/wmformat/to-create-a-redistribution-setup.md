---
title: Para criar uma configuração de redistribuição
description: Para criar uma configuração de redistribuição
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- SDK do Windows Media Format, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- SDK do Windows Media Format, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, criando
- redistribuição de software WMFDist.exe
- redistribuição, criando
- redistribuição, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159743"
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

 

 




