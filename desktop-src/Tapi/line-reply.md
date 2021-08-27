---
description: A mensagem TAPI LINE REPLY é enviada para relatar os resultados \_ de chamadas de função que foram concluídas de forma assíncrona.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: LINE_REPLY mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febe10c822a469465984b715c7b6f23d150f1f068730d4e92190b05ce50cd535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126236"
---
# <a name="line_reply-message"></a>Mensagem LINE \_ REPLY

A mensagem TAPI **LINE \_ REPLY** é enviada para relatar os resultados de chamadas de função que foram concluídas de forma assíncrona.


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

*Dwparam1* 
</dt> <dd>

O identificador de solicitação para o qual esta é a resposta.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

A indicação de êxito ou erro. O aplicativo deve transformar esse parâmetro em um LONG. Zero indica êxito; um número negativo indica um erro.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

As funções que operam de forma assíncrona retornam um valor de identificador de solicitação positivo para o aplicativo. Esse identificador de solicitação é retornado com a mensagem de resposta para identificar a solicitação que foi concluída. O outro parâmetro para a mensagem **LINE \_ REPLY** carrega a indicação de êxito ou falha. Os erros possíveis são os mesmos definidos pela função correspondente. Essa mensagem não pode ser desabilitada.

Em alguns casos, um aplicativo pode não receber a mensagem **LINE \_ REPLY** correspondente a uma chamada para uma função assíncrona. Isso ocorrerá se o alça de chamada correspondente for desaloqueado antes que a mensagem seja recebida.

> [!Note]  
> Quando um aplicativo invoca qualquer operação assíncrona que grava dados de volta na memória do aplicativo, o aplicativo deve manter essa memória disponível para escrita até que uma mensagem **LINE \_ REPLY** ou [**LINE \_ GATHERDIGITS**](line-gatherdigits.md) seja recebida.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GATHERDIGITS DE LINHA**](line-gatherdigits.md)
</dt> </dl>

 

 




