---
description: 'O método Notify notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl:: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin. Notify (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748616"
---
# <a name="ctransformoutputpinnotify-method"></a>Método CTransformOutputPin. Notify

O `Notify` método notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSelf* 
</dt> <dd>

Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro que forneceu a mensagem de controle de qualidade.

</dd> <dt>

*perguntas* 
</dt> <dd>

Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ não \_ encontrado**</dt> </dl> | Não foi possível encontrar um objeto para aceitar a mensagem.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) do filtro. Se o filtro não tratar a mensagem de qualidade, esse método chamará o método [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md) no PIN de entrada do filtro. O método **PassNotify** passa a mensagem de qualidade upstream (ou para um Gerenciador de qualidade personalizado, se um tiver sido instalado).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




