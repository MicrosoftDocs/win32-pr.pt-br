---
description: Para criar um bitmap, use a função CreateBitmap, CreateBitmapIndirect ou CreateCompatibleBitmap, CreateDIBitmap e CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Criação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038254"
---
# <a name="bitmap-creation"></a>Criação de bitmap

Para criar um bitmap, use a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Essas funções permitem que você especifique a largura e a altura, em pixels, do bitmap. A função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) também permitem que você especifique o número de planos de cores e o número de bits necessários para identificar a cor. Por outro lado, as funções [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usam um contexto de dispositivo especificado para obter o número de planos de cores e o número de bits necessários para identificar a cor.

A função [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) cria um bitmap dependente de dispositivo de um bitmap independente de dispositivo. Ele contém uma tabela de cores que descreve como os valores de pixel correspondem aos valores de cor RGB. Para obter mais informações, consulte [bitmaps dependentes de dispositivo](device-dependent-bitmaps.md) e [bitmaps independentes de dispositivo](device-independent-bitmaps.md).

Depois que o bitmap tiver sido criado, você não poderá alterar seu tamanho, o número de planos de cores ou o número de bits necessários para identificar a cor.

Quando você não precisar mais de um bitmap, chame a função [**ExcluirObjeto**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) para excluí-lo.

 

 



