---
description: A enumeração de evento do participante \_ descreve os eventos do participante.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Enumeração de PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788049"
---
# <a name="participant_event-enumeration"></a>Enumeração de evento de participante \_

\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração de **\_ evento do participante** descreve os eventos do participante. O método de [**\_ evento ITParticipantEvent:: Get**](itparticipantevent-get-event.md) retorna um membro desse enum para indicar o tipo de evento de participante de conferência que ocorreu. Essa enumeração é usada por aplicativos que acessam o [IPConf MSP](ipconf-msp.md).

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_novo \_ participante do PE**
</dt> <dd>

Um novo participante foi adicionado à conferência.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_alteração de informações do PE \_**
</dt> <dd>

As informações em um participante foram alteradas.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_sair do participante do PE \_**
</dt> <dd>

Um participante saiu da conferência.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_novo \_ Subfluxo do PE**
</dt> <dd>

Um novo substream foi adicionado ao participante.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_SUBFLUXO PE \_ removido**
</dt> <dd>

Um novo substream foi removido do participante.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**Subfluxo do PE \_ \_ mapeado**
</dt> <dd>

Um participante foi mapeado para um substream.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**Subfluxo do PE não \_ \_ mapeado**
</dt> <dd>

Um participante foi desmapeado de um substream.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_tempo limite de participante do PE \_**
</dt> <dd>

Um participante foi removido da conferência devido a um tempo limite.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**participante do PE \_ \_ recuperado**
</dt> <dd>

Um participante removido é visível novamente. Normalmente, esse é um participante que atingiu o tempo limite, mas os sinais agora estão sendo recebidos.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**participante do PE \_ \_ ativo**
</dt> <dd>

O participante se tornou ativo na conferência.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**participante do PE \_ \_ inativo**
</dt> <dd>

O participante se tornou inativo na conferência.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_comunicação local do PE \_**
</dt> <dd>

O participante local começou a falar.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**LOCAL do PE \_ \_ silencioso**
</dt> <dd>

O participante local tornou-se silencioso na conferência.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                              |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento ITParticipantEvent:: get \_**](itparticipantevent-get-event.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfaces MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




