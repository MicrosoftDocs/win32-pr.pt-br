---
description: O método Connect conclui uma conexão com o pino de saída.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Método CPullPin. Connect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768650"
---
# <a name="cpullpinconnect-method"></a>Método CPullPin. Connect

O `Connect` método conclui uma conexão com o pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do pino de saída.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador preferencial do pino de entrada ou **NULL**.

</dd> <dt>

*bSync* 
</dt> <dd>

Valor booliano que especifica se as leituras síncronas devem ser usadas. Se **for true**, o PIN executará operações de leitura síncronas no pino de saída. Se **for false**, o PIN fará solicitações de leitura assíncronas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **HRESULT**. Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                               | Descrição                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Êxito.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ já \_ conectado**</dt> </dl> | O pino de entrada já está conectado.<br/>                                  |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | O pino de saída não expõe [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método durante o processo de conexão do pino de entrada. Se o método falhar, o PIN deverá falhar na conexão.

Esse método consulta o pino de saída para a interface **IAsyncReader** . Se for bem-sucedido, ele chamará [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) para negociar o alocador para a conexão. Se o PIN de entrada tiver um alocador preferencial, especifique-o no parâmetro *pAlloc* ; o método **DecideAllocator** passa esse ponteiro para o método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) do pino de saída. Caso contrário, defina *pAlloc* como **nulo**.

Se o valor de *bSync* for **true**, o objeto **CPullPin** fará solicitações de leitura síncronas chamando o [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)do pino de saída. Caso contrário, ele chama o método [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) para fazer solicitações de leitura sobrepostas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




