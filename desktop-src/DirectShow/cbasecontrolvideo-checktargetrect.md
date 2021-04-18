---
description: O método CheckTargetRect determina se um retângulo de destino é válido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Método CBaseControlVideo. CheckTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759917"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Método CBaseControlVideo. CheckTargetRect

O `CheckTargetRect` método determina se um retângulo de destino é válido.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Ponteiro para o retângulo de destino a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna E \_ INVALIDARG se não for válido; caso contrário, retornará NOERROR (S \_ OK).

## <a name="remarks"></a>Comentários

Essa função de membro determina se o retângulo de destino solicitado é válido. Como o retângulo de destino especifica uma posição no cliente lógico da janela, as coordenadas podem ser negativas, embora a largura e a altura gerais não possam ser zero ou um valor negativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




