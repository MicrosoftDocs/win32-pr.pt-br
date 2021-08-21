---
title: Mensagens do driver
description: Mensagens do driver
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- drivers instaláveis, mensagens
- drivers instaláveis, mensagens personalizadas
- mensagens do driver
- mensagens de driver personalizado
- drivers instaláveis, função DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fb6c741cf782f620d9234f431a248fb47a8362ddcd55cf84205d8faee5800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526326"
---
# <a name="driver-messages"></a>Mensagens do driver

Cada mensagem de driver consiste em um identificador de mensagem e parâmetros de 2 32 bits. O identificador de mensagem é um valor exclusivo que a função [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) verifica para determinar qual ação executar. O significado dos parâmetros da mensagem depende da mensagem. Os parâmetros podem representar valores ou endereços. Em muitos casos, os parâmetros não são usados e são definidos como zero.

As mensagens de driver podem ser padrão ou personalizadas. Windows envia mensagens de driver padrão, como [**drv \_ OPEN**](drv-open.md), [**drv \_ CLOSE**](drv-close.md)e [**drv \_ CONFIGURE**](drv-configure.md), para um driver instalável em resposta a uma solicitação para abrir, fechar ou configurar o driver. As mensagens padrão direcionam o driver instalável para carregar ou descarregar seus recursos, habilitar ou desabilitar sua operação, abrir ou fechar uma instância de driver e exibir uma caixa de diálogo de configuração. Algumas mensagens padrão, como o [**drv \_ Power**](drv-power.md) e [**drv \_ EXITSESSION**](drv-exitsession.md), notificam o driver de eventos de todo o sistema que afetam a operação do driver ou de qualquer hardware relacionado.

Aplicativos e DLLs enviam mensagens de driver personalizadas para direcionar um driver instalável para executar ações específicas do driver. Os drivers instaláveis que dão suporte a mensagens personalizadas devem incluir o processamento apropriado na função **DriverProc** . Para evitar conflitos entre mensagens de driver personalizadas e padrão, os identificadores de mensagens personalizados devem ter valores variando de DRV \_ reservados para o \_ usuário drv. As mensagens personalizadas passadas para a função [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) são ignoradas.

 

 