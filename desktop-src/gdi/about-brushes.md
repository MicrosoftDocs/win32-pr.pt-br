---
description: 'Há dois tipos de pincéis: lógico e físico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Sobre pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c94ea9dac021a013ccc4ef624f9b00a3234102ac905999cb7c085148be91b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602786"
---
# <a name="about-brushes"></a>Sobre pincéis

Há dois tipos de pincéis: lógico e físico. Um *pincel lógico* é uma descrição do bitmap ideal que um aplicativo usa para pintar formas. Um *pincel físico* é o bitmap real que um driver de dispositivo cria com base na definição de pincel lógico de um aplicativo. Para obter mais informações sobre bitmaps, consulte [Bitmaps](bitmaps.md).

Quando um aplicativo chama uma das funções que cria um pincel, ele recupera um identificador que identifica um pincel lógico. Quando o aplicativo passa esse alça para a [**função SelectObject,**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) o driver de dispositivo para a exibição ou impressora correspondente cria o pincel físico.

Os tópicos a seguir descrevem pincéis:

-   [Origem do pincel](brush-origin.md)
-   [Tipos de pincel lógicos](logical-brush-types.md)
-   [Transferência de bloco padrão](pattern-block-transfer.md)
-   [ICM de pincel habilitadas para uso](icm-enabled-brush-functions.md)

 

 



