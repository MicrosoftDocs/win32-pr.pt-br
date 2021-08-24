---
description: A mensagem TAPI LINE CLOSE é enviada quando o dispositivo de linha especificado foi fechado \_ à força. O handle do dispositivo de linha ou quaisquer alças de chamada para chamadas na linha não são mais válidos depois que essa mensagem é enviada.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: LINE_CLOSE mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68fec993987bfc3ca36099d90eed2beadde9a749f965a36ebb6c513c210f387b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682396"
---
# <a name="line_close-message"></a>Mensagem LINE \_ CLOSE

A mensagem TAPI **LINE \_ CLOSE** é enviada quando o dispositivo de linha especificado foi fechado à força. O handle do dispositivo de linha ou quaisquer alças de chamada para chamadas na linha não são mais válidos depois que essa mensagem é enviada.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um alça para o dispositivo de linha que foi fechado. Esse alça não é mais válido.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem LINE \_ CLOSE** é enviada a qualquer aplicativo somente depois que o provedor de serviços TAPI (TSP) fechou uma linha aberta à força. Se a linha pode ou não ser reabrida imediatamente após um fechamento forçado é específica do dispositivo.

A condição causante pode ser uma alteração significativa de estado, um erro de hardware, uma perda de conexão com um servidor ou até mesmo potencialmente impedir que um único aplicativo monopolizar um dispositivo de linha por muito tempo. Um dispositivo de linha também pode ser fechado à força depois que o usuário tiver modificado a configuração dessa linha ou de seu driver. Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em vez de após a próxima reinicialização do sistema) e afetarem a exibição atual do dispositivo do aplicativo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá fechar o dispositivo de linha à força.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




