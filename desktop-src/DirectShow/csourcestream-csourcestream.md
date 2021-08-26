---
description: Construtor CSourceStream.CSourceStream – Método do construtor.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Construtor CSourceStream.CSourceStream (Source.h)
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
ms.openlocfilehash: e02827c74ef4c5461a5777221e1839846b855a4b2f4cd27d97ce913399787ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053846"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Construtor CSourceStream.CSourceStream

Método do construtor.

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

Ponteiro para uma cadeia de caracteres que contém o nome de depuração do pino.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método. Inicialize o valor como S \_ OK antes de criar o objeto . O valor será alterado somente se ocorrer um erro.

</dd> <dt>

*Pms* 
</dt> <dd>

Ponteiro para o [**filtro CSource**](csource.md) que criou esse pino.

</dd> <dt>

*Pname* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do pino.

</dd> </dl>

## <a name="remarks"></a>Comentários

A cadeia de caracteres determinada no *parâmetro pObjectName* é usada somente para fins de depuração. Para obter mais informações, [**consulte CBaseObject**](cbaseobject.md).

A cadeia de caracteres determinada no *parâmetro pName* é o nome retornado pelo [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) A `CSourceStream` classe não usa esse nome para o identificador de pino retornado pelo método [**CSourceStream::QueryId.**](csourcestream-queryid.md) Em vez **disso, QueryId** calcula um identificador de pino com base no número do pino. (Identificadores de pinos são compatíveis com persistência de grafo. Para obter mais informações, [**consulte IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)

O construtor adiciona automaticamente o pino ao filtro de propriedade chamando [**CSource::AddPin.**](csource-addpin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




