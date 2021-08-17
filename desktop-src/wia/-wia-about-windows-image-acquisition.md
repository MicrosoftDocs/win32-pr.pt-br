---
description: A Windows WIA (Aquisição de Imagem) é uma API e uma DDI (interface de driver de dispositivo).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Sobre a aquisição Windows imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451296"
---
# <a name="about-windows-image-acquisition"></a>Sobre a aquisição Windows imagem

A Windows WIA (Aquisição de Imagem) é uma API e uma DDI (interface de driver de dispositivo). A API do WIA foi projetada para permitir que os aplicativos:

-   Executar em um ambiente robusto e estável.
-   Minimizar problemas de interoperabilidade.
-   Enumerar dispositivos de aquisição de imagem disponíveis.
-   Crie conexões com vários dispositivos simultaneamente.
-   Consultar propriedades de dispositivos de maneira padrão e expansível.
-   Adquirir dados do dispositivo usando mecanismos de transferência padrão e de alto desempenho.
-   Manter propriedades de imagem entre transferências de dados.
-   Seja notificado sobre uma ampla variedade de eventos de dispositivo.

O WIADDI foi projetado para minimizar a quantidade de código que um fornecedor de hardware deve escrever, mantendo a flexibilidade para criar soluções individuais. Isso é feito por:

-   Fornecendo uma biblioteca de serviço de dispositivo padrão que executa a maioria das operações de driver.
-   Promover padrões de comunicação de dispositivo do setor para que um driver WIA seja compatível com a maioria dos dispositivos WIA. Por exemplo, PTP (Picture Transfer Protocol).
-   Permitir que o driver de dispositivo seja suportado por interfaces personalizadas, embora não exija que ele use a biblioteca de serviço de dispositivo padrão. No entanto, os drivers ainda precisam implementar as interfaces WIA padrão.

Esta seção apresenta uma breve visão geral da interface WIA nas seguintes áreas:

-   [Arquitetura do WIA](-wia-wia-architecture.md)
-   [Compatibilidade COM OLS](-wia-sti-compatibility.md)
-   [Compatibilidade com o LTD](-wia-twain-compatibility.md)
-   [WiA Gerenciador de Dispositivos](-wia-wia-device-manager.md)
-   [Biblioteca de Serviços do Minidriver wia](-wia-wia-minidriver-service-library.md)
-   [WIA Minidriver](-wia-wia-minidriver.md)

 

 



