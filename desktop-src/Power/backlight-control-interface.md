---
description: A interface de controle de luz inleve é uma interface de IOCTL padronizada para controlar o brilho da luz de LCD de cristal líquido.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interface de controle de luz Invista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756875"
---
# <a name="backlight-control-interface"></a>Interface de controle de luz Invista

A interface de controle de luz inleve é uma interface de IOCTL padronizada para controlar o brilho da luz de LCD de cristal líquido.

Aplicativos que exigem controle programático do brilho de tela de luz ou fornecem controles para que o usuário faça isso deve usar essa interface em vez de uma interface proprietária; caso contrário, o sistema não poderá consultar o brilho do hardware atual e poderá se tornar não sincronizado.

A primeira etapa é consultar o dispositivo para o brilho com suporte usando o código de controle de [**\_ \_ \_ \_ brilho com suporte da consulta de vídeo do IOCTL**](ioctl-video-query-supported-brightness.md) . Esta operação retorna um buffer que especifica os níveis de brilho disponíveis. Em seguida, você pode consultar o dispositivo para obter o brilho de vídeo atual usando a consulta de vídeo do IOCTL exibir código de controle de [**\_ \_ \_ \_ brilho**](ioctl-video-query-display-brightness.md) . Essa operação retorna as configurações atuais para o brilho atual (AC) alternado, o brilho do corrente direto (DC) e o estado de energia.

Para alterar o brilho da tela, use o [**conjunto de vídeo do IOCTL exibir código de controle de \_ \_ \_ \_ brilho**](ioctl-video-set-display-brightness.md) . Você pode definir o brilho de AC, o brilho do DC ou ambos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> </dl>

 

 



