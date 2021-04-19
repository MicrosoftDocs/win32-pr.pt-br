---
description: A mensagem TSPI LINE \_ QOSINFO faz com que a TAPI dispare um evento de QoS. Consulte ITQOSEvent para obter informações adicionais.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Mensagem de LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783364"
---
# <a name="line_qosinfo-message"></a>Mensagem de QOSINFO de linha \_

A mensagem TSPI **line \_ QOSINFO** faz com que a TAPI dispare um evento de QoS. Consulte [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) para obter informações adicionais.


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*htLine* 
</dt> <dd>

O identificador TAPI para a linha.

</dd> <dt>

*htCall* 
</dt> <dd>

O identificador TAPI para a chamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

A linha de valor \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Um membro do enumerador de [**\_ eventos de QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) que identifica o tipo de evento.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Uma constante de [tipo de mídia](./tapiprotocol--constants.md) que identifica a mídia da chamada associada a esse evento.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**evento de QOS \_**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

