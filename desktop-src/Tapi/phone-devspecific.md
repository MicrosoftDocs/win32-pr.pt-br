---
description: A TAPI envia a \_ mensagem de telefone DEVSPECIFIC para um aplicativo para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem no telefone. O significado da mensagem e a interpretação dos parâmetros são definidos pela implementação.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Mensagem de PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757615"
---
# <a name="phone_devspecific-message"></a>TELEFONE \_ DEVSPECIFIC mensagem

A TAPI envia a mensagem de **telefone \_ DEVSPECIFIC** para um aplicativo para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem no telefone. O significado da mensagem e a interpretação dos parâmetros são definidos pela implementação.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Um identificador para o dispositivo de telefone.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




