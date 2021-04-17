---
description: 'O método AlterQuality notifica o filtro de que uma alteração de qualidade é solicitada. Esse método substitui o método CTransformFilter:: AlterQuality.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Método CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752681"
---
# <a name="cvideotransformfilteralterquality-method"></a>Método CVideoTransformFilter. AlterQuality

O `AlterQuality` método notifica o filtro de que uma alteração de qualidade é solicitada. Esse método substitui o método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) .

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*perguntas* 
</dt> <dd>

Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna E \_ falha.

## <a name="remarks"></a>Comentários

Esse método é chamado quando o PIN de saída recebe uma mensagem de qualidade (por meio do método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).

O valor de atraso de *q* é armazenado na variável de membro **m \_ itrLate** . O valor de retorno de E \_ falha indica que o renderizador deve ser atualizado descartando os quadros, embora a classe **CVideoTransformFilter** também solte quadros sob as condições corretas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> <dt>

[**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




