---
description: Determina se um retângulo de origem é válido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Método CBaseControlVideo.CheckSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf7ac41d626eceee048afc4671a5e171e7164adfbd9a941b1b70bc85ea988c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873006"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>Método CBaseControlVideo.CheckSourceRect

Determina se um retângulo de origem é válido.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Ponteiro para o retângulo de origem a verificar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ INVALIDARG se não for válido; caso contrário, retorna NOERROR (S \_ OK).

## <a name="remarks"></a>Comentários

Essa função membro verifica se o retângulo de origem solicitado não excede o vídeo de origem disponível. As coordenadas esquerda e superior não podem ser negativas e a largura e a altura não podem exceder a direita e a parte inferior do vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




