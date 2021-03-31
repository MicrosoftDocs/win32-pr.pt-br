---
title: Recursos do joystick
description: Recursos do joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada de multimídia, joysticks
- joysticks, movimento de dois eixos
- joysticks, movimentação de três eixos
- joysticks, botões
- joysticks, intervalos de movimento
- joysticks, frequências de sondagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640954"
---
# <a name="joystick-capabilities"></a>Recursos do joystick

Os joysticks podem dar suporte a movimento de dois ou três eixos e até quatro botões. Os joysticks também dão suporte a diferentes intervalos de *frequências* *de movimento* e pesquisa. O intervalo de movimento é a distância que um manipulador de joystick pode mover de sua posição de repouso para a posição mais distante de sua posição de repouso. A frequência de sondagem é o intervalo de tempo entre as consultas do joystick.

Os drivers de joystick podem dar suporte a um ou dois joysticks. Você pode determinar o número de joysticks com suporte de um driver de joystick usando a função [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) . Essa função retorna um inteiro sem sinal que contém o número de joysticks com suporte ou zero se não houver suporte a um joystick. O valor de retorno não indica o número de joysticks anexados ao sistema.

Você pode determinar se um joystick está anexado ao sistema usando a função [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Essa função retornará JOYERR \_ NOERROR se o dispositivo especificado estiver anexado. Caso contrário, retornará JOYERR \_ desconectado.

Cada joystick tem vários recursos que estão disponíveis para seu aplicativo. Você pode recuperar os recursos de um joystick usando a função [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) . Essa função preenche uma estrutura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) com recursos de joystick, como os valores mínimo e máximo para seu sistema de coordenadas, o número de botões no joystick e as frequências de sondagem mínima e máxima.

 

 