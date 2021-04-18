---
description: A mensagem de fechamento de linha TAPI \_ é enviada quando o dispositivo de linha especificado é forçado a fechar. O identificador de dispositivo de linha ou qualquer identificador de chamada para chamadas na linha não será mais válido depois que essa mensagem for enviada.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Mensagem de LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788058"
---
# <a name="line_close-message"></a>Mensagem de fechamento de linha \_

A mensagem **de \_ fechamento de linha** TAPI é enviada quando o dispositivo de linha especificado é forçado a fechar. O identificador de dispositivo de linha ou qualquer identificador de chamada para chamadas na linha não será mais válido depois que essa mensagem for enviada.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para o dispositivo de linha que foi fechado. Este identificador não é mais válido.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **\_ fechamento de linha** é enviada para qualquer aplicativo somente após o provedor de serviços TAPI (TSP) ter fechado uma linha aberta de forma forçada. Se a linha pode ou não ser reaberta imediatamente após um fechamento forçado ser específico do dispositivo.

A condição de causa pode ser uma alteração significativa do estado, um erro de hardware, uma perda de conexão com um servidor ou até mesmo impedir que um único aplicativo monopolizasse um dispositivo de linha por muito tempo. Um dispositivo de linha também pode ser fechado à força após o usuário ter modificado a configuração dessa linha ou de seu driver. Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em oposição à próxima reinicialização do sistema) e afetarem a exibição atual do dispositivo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá fechar o dispositivo de linha de forma forçada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




