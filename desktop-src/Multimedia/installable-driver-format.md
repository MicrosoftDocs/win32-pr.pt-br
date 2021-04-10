---
title: Formato de driver instalável
description: Formato de driver instalável
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- drivers instaláveis, formatos
- drivers instaláveis, função DriverProc
- drivers instaláveis, mensagens
- mensagens do driver
- formatos de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294000"
---
# <a name="installable-driver-format"></a>Formato de driver instalável

Cada driver instalável exporta uma função [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) . Essa função de ponto de entrada comum recebe *mensagens de driver* do sistema que orientam o driver a realizar ações ou fornecer informações. O sistema envia mensagens de driver para a função **DriverProc** quando um aplicativo ou uma dll abre ou fecha o driver ou solicita que uma mensagem seja enviada ao driver. A função **DriverProc** processa a mensagem ou passa a mensagem para o manipulador de mensagens padrão, a função [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) . Em ambos os casos, **DriverProc** deve retornar um valor indicando se a ação solicitada foi bem-sucedida.

 

 