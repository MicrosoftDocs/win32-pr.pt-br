---
description: A \_ mensagem de resposta da linha TAPI é enviada para relatar os resultados das chamadas de função que foram concluídas de forma assíncrona.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Mensagem de LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761956"
---
# <a name="line_reply-message"></a>Mensagem de resposta de linha \_

A mensagem **de \_ resposta da linha** TAPI é enviada para relatar os resultados das chamadas de função que foram concluídas de forma assíncrona.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Retorna a instância de retorno de chamada do aplicativo.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O identificador de solicitação para o qual esta é a resposta.

</dd> <dt>

*dwParam2* 
</dt> <dd>

A indicação de êxito ou erro. O aplicativo deve converter esse parâmetro em um longo. Zero indica êxito; um número negativo indica um erro.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

As funções que operam de forma assíncrona retornam um valor de identificador de solicitação positivo para o aplicativo. Esse identificador de solicitação é retornado com a mensagem de resposta para identificar a solicitação que foi concluída. O outro parâmetro para a mensagem de **\_ resposta de linha** carrega a indicação de êxito ou falha. Os erros possíveis são os mesmos que os definidos pela função correspondente. Esta mensagem não pode ser desabilitada.

Em alguns casos, um aplicativo pode falhar ao receber a mensagem de **\_ resposta de linha** correspondente a uma chamada para uma função assíncrona. Isso ocorrerá se o identificador de chamada correspondente for desalocado antes de a mensagem ser recebida.

> [!Note]  
> Quando um aplicativo invoca qualquer operação assíncrona que grava dados de volta na memória do aplicativo, o aplicativo deve manter essa memória disponível para gravação até que uma mensagem de **\_ resposta** ou de [**linha \_ GATHERDIGITS**](line-gatherdigits.md) seja recebida.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GATHERDIGITS de linha \_**](line-gatherdigits.md)
</dt> </dl>

 

 




