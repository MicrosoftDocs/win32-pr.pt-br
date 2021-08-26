---
description: A mensagem TAPI LINE APPNEWCALLHUB é enviada para informar um aplicativo quando um novo hub de \_ chamadas foi criado.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: LINE_APPNEWCALLHUB mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf413f16270ba54fd7447cc0c41c040759edd699c995eac79314b9961486ce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905896"
---
# <a name="line_appnewcallhub-message"></a>MENSAGEM LINE \_ APPNEWCALLHUB

A mensagem TAPI **LINE \_ APPNEWCALLHUB** é enviada para informar um aplicativo quando um novo hub de chamadas foi criado.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um alça para a chamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha da chamada.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O nível de acompanhamento no novo hub, conforme definido por uma das [**\_ constantes LINECALLHUBTRACKING**](linecallhubtracking--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem se origina com TAPI em vez de com um provedor de serviços, portanto, não há nenhuma mensagem TSPI correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




