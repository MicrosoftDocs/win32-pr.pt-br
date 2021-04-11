---
description: Classificações de bitmap
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Classificações de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165097"
---
# <a name="bitmap-classifications"></a>Classificações de bitmap

Há duas classes de bitmaps:

-   DIB ( [bitmaps independentes de dispositivo](device-independent-bitmaps.md) ). O formato de arquivo DIB foi projetado para garantir que gráficos de bitmap criados usando um aplicativo possam ser carregados e exibidos em outro aplicativo, mantendo a mesma aparência que o original.

-   Os bitmaps [dependentes do dispositivo](device-dependent-bitmaps.md) (BDD), também conhecidos como bitmaps GDI, eram os únicos bitmaps disponíveis nas versões anteriores do Microsoft Windows de 16 bits (antes da versão 3,0). No entanto, conforme a tecnologia de exibição melhorou e à medida que a variedade de dispositivos de vídeo disponíveis aumentou, alguns problemas inerentes surgiram, que poderiam ser resolvidos apenas usando DIBs. Por exemplo, não havia nenhum método de armazenar (ou recuperar) a resolução do tipo de exibição no qual um bitmap foi criado, portanto, um aplicativo de desenho não pôde determinar rapidamente se um bitmap era adequado para o tipo de dispositivo de vídeo no qual o aplicativo estava sendo executado.

    Apesar desses problemas, o DDBs (também conhecido como bitmaps compatíveis) ainda é útil para melhorar o desempenho do GDI e para outras situações.

 

 



