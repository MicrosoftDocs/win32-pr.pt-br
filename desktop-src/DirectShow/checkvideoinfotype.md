---
description: A função CheckVideoInfoType verifica um tipo de mídia que contém uma estrutura de formato VIDEOINFOHEADER para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Função CheckVideoInfoType (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 4463a1edb2002f64e983a38eb4a0ace5b5289b4d47ac43c8ea27bf165138ff95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539536"
---
# <a name="checkvideoinfotype-function"></a>Função CheckVideoInfoType

A `CheckVideoInfoType` função verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.

> [!Note]  
> Essa função não garante que o tipo de mídia seja válido ou que o código que usa a estrutura seja seguro.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) para validar

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                                | Descrição                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Valor de ponteiro **nulo** .<br/> |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | Tipo de mídia inválido.<br/>     |



 

## <a name="remarks"></a>Comentários

Essa função chama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no tipo de mídia. Se o tipo de formato não for FORMAT \_ VIDEOINFO, a função retornará VFW \_ E \_ tipo \_ não \_ aceito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




