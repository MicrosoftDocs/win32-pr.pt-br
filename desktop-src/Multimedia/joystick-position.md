---
title: Posição do joystick
description: Posição do joystick
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- joysticks, posição
- joysticks, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162174"
---
# <a name="joystick-position"></a>Posição do joystick

Você pode consultar um joystick para obter informações de posição e botão usando a função [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Por exemplo, um aplicativo pode consultar o joystick para valores de posição de linha de base. A folha de propriedades do painel de controle do joystick usa essa técnica ao calibrar o joystick.

Você também pode consultar um joystick ou outro dispositivo que tenha recursos estendidos usando a função [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 