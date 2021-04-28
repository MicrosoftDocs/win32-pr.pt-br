---
description: Construtor de CDeferredCommand. CDeferredCommand-método de construtor.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Construtor CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119784"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Construtor CDeferredCommand. CDeferredCommand

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pQ* 
</dt> <dd>

Ponteiro para um objeto que expõe a interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** externa para agregação.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** retornado.

</dd> <dt>

*pUnkExecutor* 
</dt> <dd>

Ponteiro para o objeto que executará esse comando.

</dd> <dt>

*time* 
</dt> <dd>

Hora em que o comando será executado.

</dd> <dt>

*IID* 
</dt> <dd>

Ponteiro para o identificador global exclusivo (**GUID**) da interface que contém o método.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método na interface a ser chamada.

</dd> <dt>

*wFlags* 
</dt> <dd>

Contexto da invocação.

</dd> <dt>

*cArgs* 
</dt> <dd>

Número de argumentos passados.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Ponteiro para uma lista de tipos de variante de argumento.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Ponteiro para uma lista de tipo Variant retornada, se houver.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Ponteiro para o último argumento na lista de parâmetros *pDispParams* com um erro.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica se o tempo de comando adiado está em tempo de fluxo (**true**) ou tempo de apresentação (**false**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




