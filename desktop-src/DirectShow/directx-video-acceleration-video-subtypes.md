---
description: Os seguintes subtipos são usados por decodificadores que usam a DXVA (aceleração de vídeo do DirectX).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Subtipos de vídeo de aceleração de vídeo DirectX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760752"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Subtipos de vídeo de aceleração de vídeo DirectX

Os seguintes subtipos são usados por decodificadores que usam a DXVA (aceleração de vídeo do DirectX). AI44 e IA44 são superfícies com um valor de bits por pixel de 8. Há 4 bits e 4 bits de *um*. *Eu* represente um índice em uma paleta YUV de 16 entradas. *Um* representa 4 bits de informações de transparência (também conhecidas por pixel-Alpha). Portanto, as superfícies AI44 e IA44 permitem 16 cores diferentes com 16 valores de transparência diferentes ou 256 representações de pixel diferentes. Com o AI44, o alfa é armazenado no Hi-Nibble, em IA44 o alfa é armazenado no meio-Nibble. Ambos os formatos são muito úteis para imagens de subimagem de DVD e imagens Line21 e Teletext. A Microsoft prefere a versão AI44 porque é um pouco mais fácil gerar texto usando esse formato.

| Subtype            | Descrição                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Para subimagems e sobreposições de texto. Consulte a descrição anterior. |
| MEDIASUBTYPE \_ IA44 | Para subimagems e sobreposições de texto. Consulte a descrição anterior. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




