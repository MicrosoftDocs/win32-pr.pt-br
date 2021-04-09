---
description: Um dispositivo de geração de imagens é representado na aquisição de imagens do Windows (WIA) como uma árvore hierárquica de objetos de item WIA (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Usando objetos de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090490"
---
# <a name="using-wia-device-objects"></a>Usando objetos de dispositivo WIA

Um dispositivo de geração de imagens é representado na aquisição de imagens do Windows (WIA) como uma árvore hierárquica de objetos de item WIA (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ). Normalmente, a raiz dessa árvore de itens representa o próprio dispositivo, enquanto os outros itens na árvore representam imagens, para uma câmera ou regiões de verificação, para um scanner.

Os aplicativos usam o Gerenciador de dispositivos WIA para criar e enumerar dispositivos WIA. As seções a seguir explicam como criar e usar dispositivos WIA:

-   [Selecionando um dispositivo](-wia-selecting-a-device.md)
-   [Dispositivos de câmera WIA](-wia-wia-camera-devices.md)
-   [Dispositivos do scanner WIA](-wia-wia-scanner-devices.md)

 

 



