---
description: Constrói um objeto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Construtor CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789966"
---
# <a name="cmsgcmsg-constructor"></a>Construtor CMsg. CMsg

Constrói um objeto [**CMsg**](cmsg.md) .

## <a name="syntax"></a>Sintaxe


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*u* 
</dt> <dd>

Código de solicitação, definido pelo cliente da classe thread e compreendido pela função de thread de trabalho substituída.

</dd> <dt>

*dw* 
</dt> <dd>

Sinalizador de parâmetro para o código de solicitação.

</dd> <dt>

*LP* 
</dt> <dd>

Ponteiro para dados exigidos pelo thread de trabalho como valores de parâmetro ou retorno. Esses dados não devem ser baseados em pilha, pois serão referenciados algum tempo após a conclusão da operação de enfileiramento.

</dd> <dt>

*pEvent* 
</dt> <dd>

Ponteiro para o objeto de evento que um thread de trabalho pode sinalizar para indicar a conclusão da operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa função de membro contém uma solicitação para que um thread de trabalho do [**CMsgThread**](cmsgthread.md) atue. Todos os parâmetros são passados para a função de thread de trabalho como parâmetros quando essa mensagem é processada. Os significados dos parâmetros são definidos pela função de cliente que chama o thread de trabalho e a classe derivada que fornece a função de execução do thread de trabalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




