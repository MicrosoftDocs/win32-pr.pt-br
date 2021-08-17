---
description: A mensagem LINE QUEUESTATUS é enviada quando o status de uma fila ACD muda em um manipulador de agente para o qual o aplicativo \_ tem uma linha aberta no momento. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: LINE_QUEUESTATUS mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336a8239e31e5c0bcc70de747cbb48a2028c85e67f44a3e45032f02b37065d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975526"
---
# <a name="line_queuestatus-message"></a>Mensagem LINE \_ QUEUESTATUS

A **mensagem LINE \_ QUEUESTATUS** é enviada quando o status de uma fila ACD muda em um manipulador de agente para o qual o aplicativo tem uma linha aberta no momento. Essa mensagem é gerada usando a [**função lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

O alça do aplicativo para o dispositivo de linha. Isso está relacionado ao manipulador de agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O identificador da fila cujo status foi alterado.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Especifica o status da fila que foi alterado. Pode ser uma ou mais das [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Definido como zero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




