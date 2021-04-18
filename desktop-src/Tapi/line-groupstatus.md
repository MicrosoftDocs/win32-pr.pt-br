---
description: A mensagem de linha \_ GROUPSTATUS é enviada quando o status de um grupo de AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Mensagem de LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757619"
---
# <a name="line_groupstatus-message"></a>Mensagem de GROUPSTATUS de linha \_

A mensagem de **linha \_ GROUPSTATUS** é enviada quando o status de um grupo de AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


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

Reservado. Definido como zero.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica o status do grupo que foi alterado. O aplicativo pode invocar [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) para determinar as alterações nos grupos disponíveis. O parâmetro *dwParam2* é uma ou mais das [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).

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

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




