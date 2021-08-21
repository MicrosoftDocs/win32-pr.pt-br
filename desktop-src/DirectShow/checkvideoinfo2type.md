---
description: A função CheckVideoInfo2Type verifica um tipo de mídia que contém uma estrutura de formato VIDEOINFOHEADER2 para determinados erros comuns que podem causar estouros de buffer ou estouros inteiros.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Função CheckVideoInfo2Type (Checkbmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 48d9deab4d87868cbc9e5418ccd6b7e2c7e9ecf93350ad70cb6c934d365e4655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074180"
---
# <a name="checkvideoinfo2type-function"></a>Função CheckVideoInfo2Type

A função verifica um tipo de mídia que contém uma estrutura de formato `CheckVideoInfo2Type` [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) para determinados erros comuns que podem causar estouros de buffer ou estouros inteiros.

> [!Note]  
> Essa função não garante que o tipo de mídia seja válido ou que o código que usa a estrutura seja seguro.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para a estrutura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser validada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT.**



| Código de retorno                                                                                                | Descrição                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                  | **Valor do** ponteiro NULL<br/> |
| <dl> <dt>**TIPO VFW \_ E \_ NÃO \_ \_ ACEITO**</dt> </dl> | Tipo de mídia inválido<br/>     |



 

## <a name="remarks"></a>Comentários

Essa função chama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar a [**estrutura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no tipo de mídia. Se o tipo de formato não for **FORMAT \_ VideoInfo2**, a função retornará **VFW \_ E TYPE NOT \_ \_ \_ ACCEPTED**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




