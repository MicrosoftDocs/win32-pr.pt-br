---
description: A mensagem de CALLHUBCLOSE de linha TAPI \_ é enviada quando um hub de chamada é fechado.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Mensagem de LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757208"
---
# <a name="line_callhubclose-message"></a>Mensagem de CALLHUBCLOSE de linha \_

A mensagem **de \_ CALLHUBCLOSE de linha** TAPI é enviada quando um hub de chamada é fechado.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para a chamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Reservado. Defina como 0.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reservado. Defina como 0.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Defina como 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem é originada com TAPI em vez de com um provedor de serviços, portanto, não há nenhuma mensagem TSPI correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




