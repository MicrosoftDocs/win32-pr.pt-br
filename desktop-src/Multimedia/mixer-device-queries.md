---
title: Consultas de dispositivo do mixer
description: Consultas de dispositivo do mixer
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- áudio multimídia, consultas de dispositivo do mixer
- áudio, consultas de dispositivo do mixer
- mixers de áudio, consultas de dispositivo
- mixers, consultas de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007487"
---
# <a name="mixer-device-queries"></a>Consultas de dispositivo do mixer

Os serviços de mixer fornecem funções para determinar o número de dispositivos de mixer presentes no sistema e os recursos dos dispositivos. Você também pode usar uma função de serviços de mixer para determinar o identificador de dispositivo para um dispositivo de mixer.

Você pode usar a função [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) para determinar quantos dispositivos de mixer estão presentes no sistema. Os dispositivos do mixer são identificados por um identificador de dispositivo. Os identificadores de dispositivo são determinados implicitamente a partir do número de dispositivos presentes em um determinado sistema. Elas variam de zero a um menor que o número de dispositivos presentes.

Antes de usar um dispositivo de mixer, você deve determinar seus recursos. Os recursos de áudio podem variar de um computador de multimídia para outro, para que os aplicativos precisem trabalhar com uma variedade de hardwares de áudio.

Você pode usar a função [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) para determinar os recursos dos dispositivos de mixer. Essa função preenche uma estrutura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) com informações sobre os recursos de um dispositivo especificado.

A função [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera o identificador de dispositivo do mixer de áudio associado a um identificador de dispositivo especificado. Por exemplo, você pode usar essa função para recuperar o identificador de dispositivo para um mixer de áudio e, em seguida, usar o identificador do dispositivo para ajustar o volume ou para exibir outro controle.

 

 