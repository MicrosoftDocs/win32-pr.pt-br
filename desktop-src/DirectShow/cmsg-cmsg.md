---
description: Constrói um objeto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Construtor CMsg.CMsg (Msgthrd.h)
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
ms.openlocfilehash: f921c96ae185d8993002c84a09b4efb8bc5977104c274de3a2ffc964a093f1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831896"
---
# <a name="cmsgcmsg-constructor"></a>Construtor CMsg.CMsg

Constrói um [**objeto CMsg.**](cmsg.md)

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

Código de solicitação, definido pelo cliente da classe de thread e compreendido pela função de thread de trabalho substituído.

</dd> <dt>

*dw* 
</dt> <dd>

Parâmetro de sinalizador para o código de solicitação.

</dd> <dt>

*Lp* 
</dt> <dd>

Ponteiro para os dados exigidos pelo thread de trabalho como parâmetro ou valores de retorno. Esses dados não devem ser baseados em pilha, pois serão referenciados algum tempo depois de concluir a operação de en fila.

</dd> <dt>

*pEvent* 
</dt> <dd>

Ponteiro para o objeto de evento que um thread de trabalho pode sinalizar para indicar a conclusão da operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa função membro contém uma solicitação para um thread de trabalho [**CMsgThread**](cmsgthread.md) agir. Todos os parâmetros são passados para a função de thread de trabalho como parâmetros quando essa mensagem é processada. Os significados dos parâmetros são definidos pela função de cliente que chama o thread de trabalho e a classe derivada que fornece a função de execução do thread de trabalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




