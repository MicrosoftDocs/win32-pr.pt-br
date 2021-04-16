---
description: O método DecideBufferSize define os requisitos de buffer do pino de saída.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Método CTransInPlaceFilter. DecideBufferSize (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758649"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>Método CTransInPlaceFilter. DecideBufferSize

O `DecideBufferSize` método define os requisitos de buffer do pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Ponteiro para o objeto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado pelo pino de saída.

</dd> <dt>

*pProperties* 
</dt> <dd>

Ponteiro para as propriedades de alocador solicitadas para contagem, tamanho e alinhamento, conforme especificado pela estrutura de [**\_ Propriedades do alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                            | Descrição        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Sucesso<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado quando a classe **CTransInPlaceFilter** precisa fornecer um tamanho de buffer para o filtro downstream. Se o filtro **CTransInPlaceFilter** já estiver conectado ao upstream, ele usará as propriedades de alocador na conexão de PIN upstream. Caso contrário, ele define o tamanho do buffer como 1 byte como um valor de espaço reservado temporário. Quando o filtro upstream se conecta, a classe **CTransInPlaceFilter** renegocia o alocador downstream. Para obter mais informações sobre o processo de conexão de PIN nessa classe, consulte [**classe CTransInPlaceFilter**](ctransinplacefilter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




