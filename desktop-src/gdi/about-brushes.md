---
description: 'Há dois tipos de pincéis: lógico e físico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Sobre pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090979"
---
# <a name="about-brushes"></a>Sobre pincéis

Há dois tipos de pincéis: lógico e físico. Um *pincel lógico* é uma descrição do bitmap ideal que um aplicativo usa para pintar formas. Um *pincel físico* é o bitmap real que um driver de dispositivo cria com base na definição de pincel lógico de um aplicativo. Para obter mais informações sobre bitmaps, consulte [bitmaps](bitmaps.md).

Quando um aplicativo chama uma das funções que cria um pincel, ele recupera um identificador que identifica um pincel lógico. Quando o aplicativo passa esse identificador para a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , o driver de dispositivo para a exibição ou impressora correspondente cria o pincel físico.

Os tópicos a seguir descrevem os pincéis:

-   [Origem do pincel](brush-origin.md)
-   [Tipos de pincel lógico](logical-brush-types.md)
-   [Transferência de bloco de padrão](pattern-block-transfer.md)
-   [Funções de pincel habilitadas para ICM](icm-enabled-brush-functions.md)

 

 



