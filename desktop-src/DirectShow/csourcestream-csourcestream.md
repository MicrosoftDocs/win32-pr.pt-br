---
description: Construtor de CSourceStream. CSourceStream-método de construtor.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Construtor CSourceStream. CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085184"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Construtor CSourceStream. CSourceStream

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome de depuração do PIN.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método. Inicialize o valor para S \_ OK antes de criar o objeto. O valor será alterado somente se ocorrer um erro.

</dd> <dt>

*PMS* 
</dt> <dd>

Ponteiro para o filtro [**CSource**](csource.md) que criou este pin.

</dd> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do PIN.

</dd> </dl>

## <a name="remarks"></a>Comentários

A cadeia de caracteres fornecida no parâmetro *pObjectName* é usada somente para fins de depuração. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

A cadeia de caracteres fornecida no parâmetro *pname* é o nome retornado pelo método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . A `CSourceStream` classe não usa esse nome para o identificador de PIN retornado pelo método [**CSourceStream:: QueryId**](csourcestream-queryid.md) . Em vez disso, **QueryId** calcula um identificador de PIN com base no número do PIN. (Os identificadores de PIN dão suporte à persistência de gráfico. Para obter mais informações, consulte [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)

O construtor adiciona automaticamente o PIN ao filtro proprietário, chamando [**CSource:: AddPin**](csource-addpin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




