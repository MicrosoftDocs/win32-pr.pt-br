---
description: O método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757442"
---
# <a name="cbasepincheckconnect-method"></a>Método CBasePin. CheckConnect

O `CheckConnect` método determina se uma conexão de PIN é adequada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                               | Descrição                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Êxito.<br/>                           |
| <dl> <dt>**VFW \_ E \_ direção inválida \_**</dt> </dl> | As direções do PIN não são compatíveis.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado em ambos os Pins no início do processo de conexão. O PIN de conexão o chama de dentro do método [**CBasePin:: Connect**](cbasepin-connect.md) e o PIN de recebimento o chama de dentro do método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .

Use esse método para determinar se o PIN especificado pelo parâmetro *pPin* é adequado para uma conexão. A classe base retornará um erro se ambos os Pins tiverem a mesma direção (entrada ou ambas as saídas). Classes derivadas podem substituir esse método para verificar outros recursos no PIN. Por exemplo, a classe [**CBaseOutputPin**](cbaseoutputpin.md) consulta o pino de entrada para sua interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

Se esse método falhar, a conexão falhará e o PIN chamará o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Use **BreakConnect** para liberar todos os recursos obtidos no `CheckConnect` . Por exemplo, se `CheckConnect` o chamar o método **QueryInterface** , **BreakConnect** deverá liberar a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




