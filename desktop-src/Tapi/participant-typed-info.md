---
description: 'Os membros da \_ Enumeração informações digitadas do participante \_ identificam o tipo de informações do participante que estão sendo recuperadas pelo método ITParticipant:: get \_ ParticipantTypedInfo. Essa enumeração é usada por aplicativos que acessam o IPConf MSP.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Enumeração de PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de57331cd0774409118b7253fd5705879e3b3504b04b20a16aa2df269504512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100566"
---
# <a name="participant_typed_info-enumeration"></a>Enumeração de informações de \_ tipo de participante \_

\[**Participante \_ do as \_ informações digitadas** não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

Os membros da enumeração **\_ \_ informações digitadas do participante** identificam o tipo de informações do participante que estão sendo recuperadas pelo método [**ITParticipant:: get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) . Essa enumeração é usada por aplicativos que acessam o [IPConf MSP](ipconf-msp.md).

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**\_CANÔNICO PTI**
</dt> <dd>

Nome canônico do participante, como someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**nome do PTI \_**
</dt> <dd>

Nome de participante que é exibível.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**\_EmailAddress PTI**
</dt> <dd>

Endereço de email do participante.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**
</dt> <dd>

Endereço de telefone do participante.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_local PTI**
</dt> <dd>

Endereço geográfico do participante.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_ferramenta PTI**
</dt> <dd>

Aplicativo do participante.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI \_ observações**
</dt> <dd>

Observações sobre o participante.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ privado**
</dt> <dd>

Define uma extensão experimental ou de SDES (descrição de origem específica do aplicativo). Consulte RFC 1889 para obter detalhes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant:: obter \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfaces MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




