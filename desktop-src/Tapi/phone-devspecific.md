---
description: A TAPI envia a mensagem PHONE DEVSPECIFIC para um aplicativo para notificar o aplicativo sobre eventos específicos do dispositivo \_ que ocorrem no telefone. O significado da mensagem e a interpretação dos parâmetros é definido pela implementação.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578ba0960963f85ff597d9a6bc87ff3369a6c837ed58367bd82d62a13341e988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072896"
---
# <a name="phone_devspecific-message"></a>Mensagem \_ PHONE DEVSPECIFIC

A TAPI envia a **mensagem PHONE \_ DEVSPECIFIC** para um aplicativo para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem no telefone. O significado da mensagem e a interpretação dos parâmetros é definido pela implementação.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Um alça para o dispositivo de telefone.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




