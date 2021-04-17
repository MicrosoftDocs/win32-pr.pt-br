---
description: A mensagem de resposta do telefone TAPI \_ é enviada a um aplicativo para relatar os resultados da chamada de função que foi concluída de forma assíncrona.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Mensagem de PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761950"
---
# <a name="phone_reply-message"></a>Mensagem de resposta do telefone \_

A mensagem **de \_ resposta do telefone** TAPI é enviada a um aplicativo para relatar os resultados da chamada de função que foi concluída de forma assíncrona.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Não utilizado.

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

As funções que operam de forma assíncrona retornam um valor de identificador de solicitação positivo para o aplicativo. Esse identificador de solicitação é retornado com a mensagem de resposta para identificar a solicitação que foi concluída. O outro parâmetro para a mensagem de **\_ resposta do telefone** carrega a indicação de êxito ou falha. Os erros possíveis são os mesmos que os definidos pela função correspondente. Esta mensagem não pode ser desabilitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




