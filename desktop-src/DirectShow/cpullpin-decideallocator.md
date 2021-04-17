---
description: O método DecideAllocator negocia um alocador com o pino de saída.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Método CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789957"
---
# <a name="cpullpindecideallocator-method"></a>Método CPullPin. DecideAllocator

O `DecideAllocator` método negocia um alocador com o pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador preferencial do pino de entrada ou **NULL**.

</dd> <dt>

*pProps* 
</dt> <dd>

Ponteiro para uma estrutura [**de \_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) opcional que contém os requisitos de buffer do pino de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.

## <a name="remarks"></a>Comentários

Esse método chama o método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) para negociar um alocador. Ele passa o parâmetro *pAlloc* diretamente para o método **RequestAllocator** . Ele passa o parâmetro *pProps* para **RequestAllocator** se *pProps* não for **nulo**; caso contrário, ele cria uma estrutura de **\_ Propriedades de alocador** com uma solicitação padrão de três buffers de 64K.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> <dt>

[**CPullPin:: conectar**](cpullpin-connect.md)
</dt> </dl>

 

 




