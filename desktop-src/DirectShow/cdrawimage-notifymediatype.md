---
description: O método NotifyMediaType notifica o objeto CDrawImage do tipo de mídia atual.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Método CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770101"
---
# <a name="cdrawimagenotifymediatype-method"></a>Método CDrawImage. NotifyMediaType

O `NotifyMediaType` método notifica o objeto **CDrawImage** do tipo de mídia atual.

## <a name="syntax"></a>Sintaxe


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) ou **NULL** para limpar o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro proprietário deve chamar esse método sempre que o tipo de mídia for alterado. Normalmente, isso ocorre quando o PIN se conecta pela primeira vez e após uma alteração de formato dinâmico.

O objeto **CDrawImage** armazena o ponteiro *pMediaType* na variável de membro **m \_ pMediaType** . Portanto, se o chamador precisar liberar o objeto **CMediaType** , ele deverá atualizar o objeto **CDrawImage** chamando esse método novamente, seja com um novo ponteiro ou com um valor **nulo** . Caso contrário, poderá ocorrer um erro quando o objeto **CDrawImage** tentar referenciar o ponteiro antigo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




