---
description: Método CBasePin.CheckConnect – o método CheckConnect determina se uma conexão de pino é adequada.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin.CheckConnect (Amfilter.h)
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
ms.openlocfilehash: 0a91e936f13c76ed4d99d7c5048820777afa47c9a52c260bb7f34acb702cb777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916846"
---
# <a name="cbasepincheckconnect-method"></a>Método CBasePin.CheckConnect

O `CheckConnect` método determina se uma conexão de pino é adequada.

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

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                               | Descrição                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Êxito.<br/>                           |
| <dl> <dt>**VFW \_ E \_ DIREÇÃO \_ INVÁLIDA**</dt> </dl> | As direções de pino não são compatíveis.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado em ambos os pinos no início do processo de conexão. O pino de conexão chama-o de dentro do método [**CBasePin::Conexão**](cbasepin-connect.md) e o pin receptor o chama de dentro do [**método CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)

Use esse método para determinar se o pino especificado pelo parâmetro *pPin* é adequado para uma conexão. A classe base retornará um erro se ambos os pinos têm a mesma direção (entrada ou ambas as saídas). As classes derivadas podem substituir esse método para verificar outros recursos no pin. Por exemplo, a [**classe CBaseOutputPin**](cbaseoutputpin.md) consulta o pino de entrada para sua interface [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

Se esse método falhar, a conexão falhará e o pino chamará o [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Use **BreakConnect** para liberar todos os recursos obtidos no `CheckConnect` . Por exemplo, se `CheckConnect` chamar o **método QueryInterface,** **BreakConnect** deverá liberar a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




