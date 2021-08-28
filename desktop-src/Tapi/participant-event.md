---
description: A enum \_ EVENTO PARTICIPANTE descreve os eventos do participante.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: PARTICIPANT_EVENT enumeração (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5eb7a98a445ecb89b25fe2d18ef77be31aa54b5fac2920814fba2c4a3f6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959766"
---
# <a name="participant_event-enumeration"></a>\_Enumeração PARTICIPANT EVENT

\[Essa enumeração não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A **enum \_ EVENTO PARTICIPANTE** descreve os eventos do participante. O [**método ITParticipantEvent::get \_ Event**](itparticipantevent-get-event.md) retorna um membro dessa enum para indicar o tipo de evento de participante de conferência que ocorreu. Essa enum é usada por aplicativos que acessam [o IPConf MSP.](ipconf-msp.md)

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**NOVO \_ PARTICIPANTE DO PE \_**
</dt> <dd>

Um novo participante foi adicionado à conferência.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**ALTERAÇÃO DE INFORMAÇÕES DO PE \_ \_**
</dt> <dd>

As informações sobre um participante foram alteradas.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE \_ PARTICIPANT \_ LEAVE**
</dt> <dd>

Um participante saiu da conferência.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE \_ NEW \_ SUBSTREAM**
</dt> <dd>

Um novo substream foi adicionado ao participante.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**SUBSTREAM PE \_ \_ REMOVIDO**
</dt> <dd>

Um novo substream foi removido do participante.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**\_PE SUBSTREAM \_ MAPEADO**
</dt> <dd>

Um participante foi mapeado para um substream.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE \_ SUBSTREAM \_ UNMAPPED**
</dt> <dd>

Um participante foi não mapeado de um substream.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE \_ PARTICIPANT \_ TIMEOUT**
</dt> <dd>

Um participante foi removido da conferência devido a um tempoout.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PARTICIPANTE \_ PE \_ RECUPERADO**
</dt> <dd>

Um participante removido fica visível novamente. Normalmente, esse é um participante que teve o tempo de vida, mas os sinais agora estão sendo recebidos.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PARTICIPANTE DO PE \_ \_ ATIVO**
</dt> <dd>

O participante se tornou ativo na conferência.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE \_ PARTICIPANT \_ INACTIVE**
</dt> <dd>

O participante se tornou inativo na conferência.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE \_ LOCAL \_ TALKING**
</dt> <dd>

O participante local começou a falar.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ LOCAL \_ SILENT**
</dt> <dd>

O participante local se tornou silencioso na conferência.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                              |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento ITParticipantEvent::get \_**](itparticipantevent-get-event.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP Interfaces](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




