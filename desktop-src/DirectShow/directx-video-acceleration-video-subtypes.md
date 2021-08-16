---
description: Os subtipos a seguir são usados por decodificadores que estão usando a DXVA (Aceleração de Vídeo DirectX).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Subtipos de vídeo de aceleração de vídeo do DirectX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a2197d504929e001e07fb1ac107dbd7b13b1f443e43ec8ed90232372b08f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016143"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Subtipos de vídeo de aceleração de vídeo do DirectX

Os subtipos a seguir são usados por decodificadores que estão usando a DXVA (Aceleração de Vídeo DirectX). AI44 e IA44 são superfícies com um valor de bits por pixel de 8. Há 4 bits de I e 4 bits de *A.* *Representa* um índice em uma paleta YUV de 16 entradas. *Um* representa 4 bits de informações de transparência (também conhecidas como por pixel alfa). Portanto, as superfícies IA44 e IA44 permitem 16 cores diferentes em 16 valores de transparência diferentes ou 256 representações de pixel diferentes. Com a IA44, o alfa é armazenado no hi-nibble, em IA44, o alfa é armazenado no lo-nibble. Ambos os formatos são muito úteis para imagens de sub-imagem de DVD e imagens Line21 e Teletext. A Microsoft prefere a versão AI44 porque é um pouco mais fácil gerar texto usando esse formato.

| Subtype            | Descrição                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Para subpicture e sobreposições de texto. Consulte a descrição anterior. |
| MEDIASUBTYPE \_ IA44 | Para subpicture e sobreposições de texto. Consulte a descrição anterior. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




