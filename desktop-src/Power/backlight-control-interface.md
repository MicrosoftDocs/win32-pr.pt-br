---
description: A interface de controle de luz de fundo é uma interface IOCTL padronizada para controlar o brilho da luz de fundo do LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interface de controle de luz de fundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a6a82cede03d18f9d237bab09a590f9bcdc0da86651dacd0912357c32d36ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143719"
---
# <a name="backlight-control-interface"></a>Interface de controle de luz de fundo

A interface de controle de luz de fundo é uma interface IOCTL padronizada para controlar o brilho da luz de fundo do LCD.

Os aplicativos que exigem controle programático do brilho da luz de fundo ou fornecem controles para que o usuário faça isso devem usar essa interface em vez de uma interface proprietária; caso contrário, o sistema não poderá consultar o brilho do hardware atual e poderá se tornar não sincronizado.

A primeira etapa é consultar o dispositivo quanto ao brilho com suporte usando o código de controle [**IOCTL \_ VIDEO \_ QUERY \_ \_ SUPPORTED BRIGHTNESS.**](ioctl-video-query-supported-brightness.md) Essa operação retorna um buffer que especifica os níveis de brilho disponíveis. Em seguida, você pode consultar o dispositivo quanto ao brilho de exibição atual usando o código de controle [**IOCTL \_ VIDEO \_ QUERY \_ DISPLAY \_ BRIGHTNESS.**](ioctl-video-query-display-brightness.md) Essa operação retorna as configurações atuais para o brilho atual alternado (AC), o brilho direto atual (DC) e o estado de energia.

Para alterar o brilho da exibição, use o código [**de controle IOCTL \_ VIDEO SET DISPLAY \_ \_ \_ BRIGHTNESS.**](ioctl-video-set-display-brightness.md) Você pode definir o brilho ac, o brilho do DC ou ambos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciamento de Energia](about-power-management.md)
</dt> </dl>

 

 



