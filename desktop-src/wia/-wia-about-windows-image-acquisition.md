---
description: A interface de aquisição de imagens do Windows (WIA) é uma API e uma DDI (interface de driver de dispositivo).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Sobre a aquisição de imagens do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772510"
---
# <a name="about-windows-image-acquisition"></a>Sobre a aquisição de imagens do Windows

A interface de aquisição de imagens do Windows (WIA) é uma API e uma DDI (interface de driver de dispositivo). A API WIA foi projetada para permitir que os aplicativos:

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

 

 



