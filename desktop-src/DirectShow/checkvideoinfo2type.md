---
description: A função CheckVideoInfo2Type verifica um tipo de mídia que contém uma estrutura de formato VIDEOINFOHEADER2 para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Função CheckVideoInfo2Type (Checkbmi. h)
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
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786993"
---
# <a name="checkvideoinfo2type-function"></a>Função CheckVideoInfo2Type

A `CheckVideoInfo2Type` função verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.

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

*PMT* 
</dt> <dd>

Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser validada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                                | Descrição                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Sucesso<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Valor de ponteiro **nulo**<br/> |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | Tipo de mídia inválido<br/>     |



 

## <a name="remarks"></a>Comentários

Essa função chama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no tipo de mídia. Se o tipo de formato não for **Format \_ VideoInfo2**, a função retornará **VFW \_ E \_ tipo \_ não \_ aceito**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




