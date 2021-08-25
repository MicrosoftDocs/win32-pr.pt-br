---
description: A mensagem \_ QOSINFO TSPI LINE faz com que a TAPI a fire um evento QOS. Consulte ITQOSEvent para obter informações adicionais.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: LINE_QOSINFO mensagem (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e6273eb31447f0e0c9543dfa191a25869fa08f05be8a5c639ceb101deff47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873316"
---
# <a name="line_qosinfo-message"></a>Mensagem \_ LINE QOSINFO

A mensagem **\_ QOSINFO TSPI LINE** faz com que a TAPI a fire um evento QOS. Consulte [**ITQOSEvent para**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) obter informações adicionais.


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*htLine* 
</dt> <dd>

O alça tapi para a linha.

</dd> <dt>

*Htcall* 
</dt> <dd>

O alça tapi para a chamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

O valor LINE \_ QOSINFO.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Um membro do [**enumerador \_ QOS EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) que identifica o tipo de evento.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Uma [constante de tipo](./tapiprotocol--constants.md) de mídia que identifica a mídia da chamada associada a esse evento.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EVENTO \_ QOS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

