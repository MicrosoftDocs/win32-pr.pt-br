---
description: Para criar um bitmap, use a função CreateBitmap, CreateBitmapIndirect ou CreateCompatibleBitmap, CreateDIBitmap e CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Criação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165096"
---
# <a name="bitmap-creation"></a>Criação de bitmap

Para criar um bitmap, use a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Essas funções permitem que você especifique a largura e a altura, em pixels, do bitmap. A função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) também permitem que você especifique o número de planos de cores e o número de bits necessários para identificar a cor. Por outro lado, as funções [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usam um contexto de dispositivo especificado para obter o número de planos de cores e o número de bits necessários para identificar a cor.

A função [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) cria um bitmap dependente de dispositivo de um bitmap independente de dispositivo. Ele contém uma tabela de cores que descreve como os valores de pixel correspondem aos valores de cor RGB. Para obter mais informações, consulte [bitmaps dependentes de dispositivo](device-dependent-bitmaps.md) e [bitmaps independentes de dispositivo](device-independent-bitmaps.md).

Depois que o bitmap tiver sido criado, você não poderá alterar seu tamanho, o número de planos de cores ou o número de bits necessários para identificar a cor.

Quando você não precisar mais de um bitmap, chame a função [**ExcluirObjeto**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) para excluí-lo.

 

 



