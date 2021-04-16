---
description: A mensagem de APPNEWCALLHUB de linha TAPI \_ é enviada para informar um aplicativo quando um novo hub de chamadas tiver sido criado.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Mensagem de LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759464"
---
# <a name="line_appnewcallhub-message"></a>Mensagem de APPNEWCALLHUB de linha \_

A mensagem **de \_ APPNEWCALLHUB de linha** TAPI é enviada para informar um aplicativo quando um novo hub de chamadas tiver sido criado.


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

O nível de rastreamento no novo hub, conforme definido por uma das [**\_ constantes LINECALLHUBTRACKING**](linecallhubtracking--constants.md).

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



 

 




