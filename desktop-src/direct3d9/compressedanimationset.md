---
description: Contém dados de conjunto de animação.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0666a7aa62eda365eceba1f016af14c3f84c47c39257d42e287ced470bff7f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097084"
---
# <a name="compressedanimationset"></a>CompressedAnimationSet

Contém dados de conjunto de animação.

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

Em que:

-   CompressedBlockSize-tamanho total, em bytes, dos dados compactados no buffer de dados de animação do quadro chave compactado.
-   TicksPerSec-número de tiques de quadros-chave de animação que ocorrem por segundo.
-   Reproduztype-tipo do loop de reprodução do conjunto de animações. Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).
-   BufferLength-tamanho mínimo do buffer, em bytes, necessário para manter dados de animação de quadro chave compactados. Valor é igual a ((CompressedBlockSize + 3)/4).
-   CompressedData \[ BufferLength \] -uma matriz de valores de dados compactados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**XFILECOMPRESSEDANIMATIONSET**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
