---
description: 'O método ReceiveCanBlock determina se as chamadas para o método IMemInputPin:: Receive podem ser bloqueadas. Esse método implementa o método IMemInputPin:: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Método CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ece7243c145d34ed06e29b2a29ae9847e682981337b96a47976c20eb76272d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823848"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>Método CBaseInputPin. ReceiveCanBlock

O `ReceiveCanBlock` método determina se as chamadas para o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) podem ser bloqueadas. Esse método implementa o método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . O valor possível incluem os listados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O PIN não será bloqueado em uma chamada para **Receive**.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | O PIN pode ser bloqueado em uma chamada para **Receive**.<br/>    |



 

## <a name="remarks"></a>Comentários

Retorna S \_ false se as chamadas para o método **Receive** estiverem garantidas por não bloquear. Caso contrário, retorne S \_ OK ou um código de erro. Se o método **Receive** chamar **Receive** em um PIN downstream, o PIN downstream poderá ser bloqueado; `ReceiveCanBlock` deve levar esse fator em conta.

Um filtro upstream pode usar esse método para determinar sua estratégia de Threading. Se o método **Receive** puder ser bloqueado, o filtro upstream poderá decidir usar um thread de trabalho que armazena os dados em buffer. Consulte a classe [**COutputQueue**](coutputqueue.md) para uma implementação dessa estratégia.

Na classe base, esse método retorna S \_ OK quando qualquer uma das seguintes opções for verdadeira:

-   O filtro não tem nenhum pino de saída.
-   Um PIN de entrada conectado a esse filtro sinaliza que ele pode bloquear.
-   Um PIN de entrada conectado a este filtro não oferece suporte à interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




