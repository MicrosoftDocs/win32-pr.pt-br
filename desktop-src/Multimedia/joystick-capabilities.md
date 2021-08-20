---
title: Funcionalidades do Conector
description: Funcionalidades do Conector
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada multimídia, usbs
- movimento de dois eixos
- movimento de três eixos de 3 eixos
- buttons,buttons
- interpolações, intervalos de movimento
- porões, frequências de sondagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311109468485a8174d9567516e747ef786019cc105c378ee91b55fa2f123c5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140444"
---
# <a name="joystick-capabilities"></a>Funcionalidades do Conector

Os botões podem dar suporte à movimentação de dois ou três eixos e até quatro botões. Os detectores também são *suportados por diferentes intervalos de frequências* de movimento *e sondagem.* O intervalo de movimento é a distância que uma alça de guid pode mover de sua posição de posição para a posição mais distante de sua posição de posição. A frequência de sondagem é o intervalo de tempo entre as consultas de botão.

Os drivers de drivers Dols podem dar suporte a um ou dois drivers. Você pode determinar o número de vezes que há suporte para um driver de driver [**de driver de driver dogetnumdevs usando a funçãogetGetNumDevs.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) Essa função retornará um inteiro sem sinal que contém o número de nós com suporte ou zero se não houver suporte para o joystick. O valor de retorno não indica o número de botões anexados ao sistema.

Você pode determinar se um ltda está anexado ao sistema usando a [**funçãogetPos.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) Essa função retornará UM \_ NOERROR SE o dispositivo especificado estiver anexado. Caso contrário, ele retornará AOISERR \_ UNPLUGGED.

Cada recurso tem vários recursos disponíveis para seu aplicativo. Você pode recuperar as funcionalidades de um joystick usando a [**funçãogetDevCaps.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) Essa função preenche uma estrutura [**DECAPS com**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) funcionalidades de mouse, como os valores mínimo e máximo para seu sistema de coordenadas, o número de botões no botão e as frequências de sondagem mínimas e máximas.

 

 