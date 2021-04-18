---
description: A mensagem de fechamento de telefone TAPI \_ é enviada quando um dispositivo de telefone aberto é forçado a ser fechado como parte da reclamação de recurso. O identificador do dispositivo não será mais válido depois que essa mensagem for enviada.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Mensagem de PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810126"
---
# <a name="phone_close-message"></a>Mensagem de fechamento do telefone \_

A mensagem **de \_ fechamento de telefone** TAPI é enviada quando um dispositivo de telefone aberto é forçado a ser fechado como parte da reclamação de recurso. O identificador do dispositivo não será mais válido depois que essa mensagem for enviada.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Um identificador para o dispositivo de telefone aberto que foi fechado. O identificador não é mais válido depois que esta mensagem foi enviada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada do aplicativo que forneceu ao abrir o dispositivo de telefone.

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

A mensagem de **\_ fechamento do telefone** é enviada somente a um aplicativo depois que um telefone aberto é forçado a ser fechado. Isso pode ser feito para impedir que um único aplicativo monopolizasse um dispositivo de telefone por muito tempo. Se o telefone pode ser reaberto imediatamente após um fechamento forçado é específico do dispositivo.

Um dispositivo de telefone aberto também pode ser fechado à força após o usuário ter modificado a configuração desse telefone ou de seu driver. Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em vez de após a próxima reinicialização do sistema) e essas alterações afetarem a exibição atual do dispositivo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá forçar o fechamento do dispositivo telefônico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




