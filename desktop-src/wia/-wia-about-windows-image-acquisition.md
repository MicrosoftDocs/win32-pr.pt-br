---
description: a interface de aquisição de imagem de Windows (WIA) é uma API e uma DDI (interface de driver de dispositivo).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: sobre a aquisição de imagem de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451296"
---
# <a name="about-windows-image-acquisition"></a>sobre a aquisição de imagem de Windows

a interface de aquisição de imagem de Windows (WIA) é uma API e uma DDI (interface de driver de dispositivo). A API WIA foi projetada para permitir que os aplicativos:

-   Execute em um ambiente robusto e estável.
-   Minimizar problemas de interoperabilidade.
-   Enumere os dispositivos de aquisição de imagem disponíveis.
-   Crie conexões a vários dispositivos simultaneamente.
-   Consultar Propriedades de dispositivos de maneira padrão e expansível.
-   Adquira dados de dispositivo usando mecanismos de transferência padrão e de alto desempenho.
-   Manter Propriedades de imagem entre transferências de dados.
-   Seja notificado sobre uma ampla variedade de eventos de dispositivo.

O WIADDI foi projetado para minimizar a quantidade de código que um fornecedor de hardware deve escrever, mantendo a flexibilidade para criar soluções individuais. Isso é feito por:

-   Fornecer uma biblioteca de serviço de dispositivo padrão que executa a maioria das operações de driver.
-   Promover padrões de comunicação de dispositivos do setor para que um driver WIA dê suporte à maioria dos dispositivos WIA. Por exemplo, o PTP (protocolo de transferência de imagem).
-   Permitir que o driver de dispositivo dê suporte a interfaces personalizadas, embora não exija que ela use a biblioteca de serviço de dispositivo padrão. No entanto, os drivers ainda precisam implementar as interfaces WIA padrão.

Esta seção apresenta uma breve visão geral da interface WIA nas seguintes áreas:

-   [Arquitetura WIA](-wia-wia-architecture.md)
-   [Compatibilidade do STI](-wia-sti-compatibility.md)
-   [Compatibilidade com TWAIN](-wia-twain-compatibility.md)
-   [Gerenciador de Dispositivos WIA](-wia-wia-device-manager.md)
-   [Biblioteca de serviço minidriver WIA](-wia-wia-minidriver-service-library.md)
-   [Minidriver WIA](-wia-wia-minidriver.md)

 

 



