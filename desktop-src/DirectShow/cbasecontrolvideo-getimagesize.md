---
description: O método getimageize recupera informações de tamanho de imagem de vídeo.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Método CBaseControlVideo. getimageize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782853"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>Método CBaseControlVideo. getimageize

O `GetImageSize` método recupera informações de tamanho da imagem de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) a ser preenchida.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Ponteiro para o tamanho do buffer de vídeo.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Ponteiro para as dimensões de retângulo do vídeo de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                  | Descrição                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>       | Falha.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido. O formato de dados não é compatível.<br/>           |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Ocorreu um erro inesperado. Um ou mais argumentos são **nulos**.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Êxito.<br/>                                                       |



 

## <a name="remarks"></a>Comentários

Essa função de membro é uma função auxiliar usada para criar processamentos de imagem de memória de imagens DIB. Ele é chamado da implementação da classe base de [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) quando um parâmetro _pVideoImage_ **nulo** é passado para essa função de membro. Como resultado, essa função de membro constrói e retorna uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , usando as informações em *pBufferSize* e *pSourceRect*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




