---
description: A mensagem LINE GROUPSTATUS é enviada quando o status de um grupo ACD muda em um manipulador de agente para o qual o aplicativo \_ tem uma linha aberta no momento. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: LINE_GROUPSTATUS mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c70ba4badd27b4d42774549b4778bd77dda13f0ae7245ee6852c2b3afab164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761939"
---
# <a name="line_groupstatus-message"></a>Mensagem LINE \_ GROUPSTATUS

A **mensagem LINE \_ GROUPSTATUS** é enviada quando o status de um grupo ACD muda em um manipulador de agente para o qual o aplicativo tem uma linha aberta no momento. Essa mensagem é gerada usando a [**função lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


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

Reservado. Definido como zero.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Especifica o status do grupo que foi alterado. O aplicativo pode invocar [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) para determinar as alterações em grupos disponíveis. O *parâmetro dwParam2* é uma ou mais das [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).

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

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




