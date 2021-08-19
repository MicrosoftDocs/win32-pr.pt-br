---
description: o sistema operacional Microsoft Windows fornece suporte para uma variedade de dispositivos de hardware e protocolos de tempo de rede usando a arquitetura do provedor de tempo.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f2073e94bdf893793b4ae1df2974226aa197de4ff429be9ce8f2a2e4b5f597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957900"
---
# <a name="time-provider"></a>Provedor de tempo

o sistema operacional Microsoft Windows fornece suporte para uma variedade de dispositivos de hardware e protocolos de tempo de rede usando a arquitetura do *provedor de tempo* . Provedores de tempo de entrada recuperam carimbos de data/hora precisos do hardware ou da rede, e provedores de tempo de saída fornecem carimbos de data/hora para outros clientes na rede.

Os provedores de tempo são gerenciados pelo *Gerenciador de provedores de tempo*. Ele é responsável por carregar, iniciar e parar provedores de tempo conforme orientado pelo Gerenciador de controle de serviços. Essa interface torna mais fácil escrever um provedor de tempo do que escrever um serviço completo.

-   [Criando um provedor de tempo](creating-a-time-provider.md)
-   [Registrando um provedor de tempo](registering-a-time-provider.md)
-   [Provedor de tempo de exemplo](sample-time-provider.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Tempo do Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



