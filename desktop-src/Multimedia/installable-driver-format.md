---
title: Formato de driver instalável
description: Formato de driver instalável
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- drivers instaláveis, formatos
- drivers instaláveis, função DriverProc
- drivers instaláveis, mensagens
- mensagens de driver
- formatos de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c02f6bb2515d1f182146b84b7f0b971fa4b73fe2e2caf5abf63dfd4ddb272df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140785"
---
# <a name="installable-driver-format"></a>Formato de driver instalável

Cada driver instalável exporta uma [função DriverProc.](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) Essa função comum de ponto de entrada recebe mensagens *de driver* do sistema que direcionam o driver para executar ações ou fornecer informações. O sistema envia mensagens de driver para a função **DriverProc** quando um aplicativo ou DLL abre ou fecha o driver ou solicita que uma mensagem seja enviada ao driver. A **função DriverProc** processa a mensagem ou passa a mensagem para o manipulador de mensagens padrão, [a função DefDriverProc.](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) Em ambos os casos, **DriverProc** deve retornar um valor que indica se a ação solicitada foi bem-sucedida.

 

 