---
description: Para copiar um bitmap em um paralelogramo; Use a função PlgBlt, que executa uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem para um paralelogramo em um contexto de dispositivo de destino.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Rotação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988843"
---
# <a name="bitmap-rotation"></a>Rotação de bitmap

Para copiar um bitmap em um paralelogramo; Use a função [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) , que executa uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem para um paralelogramo em um contexto de dispositivo de destino. Para girar o bitmap, um aplicativo deve fornecer as coordenadas, em unidades mundiais, a serem usadas para os cantos do paralelogramo. (Para obter mais informações sobre rotação e unidades mundiais, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).)

 

 



