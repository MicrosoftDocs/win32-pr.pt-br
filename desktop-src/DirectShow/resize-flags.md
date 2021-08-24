---
description: Esses sinalizadores especificam como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Redimensionar sinalizadores (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: c38f4b1913eb7676832374e57e4d65e14dc87831c13f3cdb0de96edf9b83ebec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747097"
---
# <a name="resize-flags"></a>Redimensionar sinalizadores

\[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

Esses sinalizadores especificam como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.



| Constante/valor                                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt> </dl>                                                                          | A imagem é ampliada para se ajustar ao tamanho do quadro de destino em ambas as dimensões, sem preservar a taxa de proporção.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_ CORTAR**</dt> <dt>1</dt> </dl>                                                                                   | A imagem não foi redimensionada. Se a imagem for menor do que o quadro de destino, a área ao redor será preta. Se a imagem for maior que o quadro de destino, a imagem será cortada.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | A imagem é redimensionada para se ajustar ao quadro de destino ao longo de uma dimensão, preservando a taxa de proporção. Se a taxa de largura para altura na imagem não corresponder à taxa no quadro de destino, ela criará um letterbox.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt> </dl> | A imagem é redimensionada para preencher o quadro de destino inteiro, preservando a taxa de proporção. Em vez de criar um Letterbox, esse modo corta a imagem, seja ao longo dos lados ou entre as partes superior e inferior.<br/>                 |



## <a name="remarks"></a>Comentários

As imagens a seguir mostram os efeitos desses sinalizadores.

![redimensionar sinalizadores](images/stretch14.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineSrc:: getstretchmode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc:: setalongamode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




