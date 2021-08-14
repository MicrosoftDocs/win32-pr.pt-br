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
ms.openlocfilehash: 03c45979437c153e70aea16c6b6e48b052b0d84491dcd1880075c66c77c777d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822221"
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
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




