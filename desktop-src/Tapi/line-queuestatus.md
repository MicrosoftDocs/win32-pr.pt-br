---
description: A \_ mensagem statusfila de linha é enviada quando o status de uma fila AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Mensagem de LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779902"
---
# <a name="line_queuestatus-message"></a>Mensagem de statusfila de linha \_

A **mensagem \_ Statusfila de linha** é enviada quando o status de uma fila AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha. Isso está relacionado ao manipulador do agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O identificador da fila cujo status foi alterado.

</dd> <dt>

*dwParam2* 
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
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




