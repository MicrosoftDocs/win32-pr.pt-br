---
description: O sistema operacional Microsoft Windows oferece suporte a uma variedade de dispositivos de hardware e protocolos de tempo de rede usando a arquitetura de provedor de tempo.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829520"
---
# <a name="time-provider"></a>Provedor de tempo

O sistema operacional Microsoft Windows oferece suporte a uma variedade de dispositivos de hardware e protocolos de tempo de rede usando a arquitetura de *provedor de tempo* . Provedores de tempo de entrada recuperam carimbos de data/hora precisos do hardware ou da rede, e provedores de tempo de saída fornecem carimbos de data/hora para outros clientes na rede.

Os provedores de tempo são gerenciados pelo *Gerenciador de provedores de tempo*. Ele é responsável por carregar, iniciar e parar provedores de tempo conforme orientado pelo Gerenciador de controle de serviços. Essa interface torna mais fácil escrever um provedor de tempo do que escrever um serviço completo.

-   [Criando um provedor de tempo](creating-a-time-provider.md)
-   [Registrando um provedor de tempo](registering-a-time-provider.md)
-   [Provedor de tempo de exemplo](sample-time-provider.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Tempo do Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



