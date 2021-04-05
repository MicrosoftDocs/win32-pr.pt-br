---
title: BITS_COST_STATE (Bits5 \_ 0. h)
description: A enumeração de estado de custo do BITS \_ \_ define os valores constantes que especificam o estado de custo do bits.
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: 88fb0b949fb06a6e1eb6e14cdf55c8d54d9ab33c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918567"
---
# <a name="bits_cost_state"></a>\_estado de custo do bits \_

Define constantes que especificam o estado de custo do BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**Estado de custo do BITS \_ \_ \_ irrestrito**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**\_ \_ \_ \_ uso \_ desconhecido do estado de custo do bits**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**Estado de custo do BITS \_ \_ abaixo do \_ \_ limite**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**Estado de custo do BITS \_ \_ perto do \_ \_ limite**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**OVERCAP de estado de custo do BITS \_ \_ \_ \_ cobrado**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**Estado de custo do BITS \_ \_ \_ OVERCAP \_ limitado**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**\_ \_ \_ uso \_ baseado no estado de custo do bits**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**opção de custo de BITS \_ \_ \_ ignorar \_ congestionamento**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**Estado de custo do BITS \_ \_ \_ reservado**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**transferência de estado de custo do BITS \_ \_ \_ \_ não \_ móvel**
</dt> <dd> <dl> <dt>

(BITS \_ opção de custo ignorar o uso do estado de custo dos bits de \_ \_ \_ congestionamento \| \_ \_ \_ \_ com base no \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ estado de custo do bits OVERCAP limitação do estado de custo do bits de débito OVERCAP do estado de custo de bits de limite inferior do estado do custo do bit do bits limitado, estado de custo do bits desconhecido 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**transferência de estado de custo de BITS \_ \_ \_ \_ sem \_ sobretaxa**
</dt> <dd> <dl> <dt>

(BITS \_ opção de custo ignorar o uso do estado de custo de bits de congestionamento com base no estado de custo do bits com limite OVERCAP de custo de bits restrito estado de custo de bits de extremidade inferior abaixo da Cap estado de custo de bits \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ limitado \_ uso \_ desconhecido \| bits \_ \_ estado custo \_ irrestrito
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**\_padrão de \_ transferência de estado de custo do bits \_ \_**
</dt> <dd> <dl> <dt>

(BITS \_ opção de custo ignorar o uso do estado de custo dos bits de congestionamento com base no estado de custo do bits \_ \_ \_ \| \_ \_ \_ \_ com \| limite de \_ \_ \_ OVERCAP \_ bits limitado \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ estado de custo de bits restritos estado de custo do bit de bits desconhecido 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**transferência de estado de custo do BITS sem \_ \_ \_ \_ restrições**
</dt> <dd> <dl> <dt>

(BITS \_ opção de custo \_ ignorar o estado de custo de bits de \_ \_ congestionamento \| \_ \_ \_ OVERCAP limite de custo de \_ \| bits \_ \_ \_ restritos
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**transferência de estado de custo do BITS \_ \_ \_ \_ sempre**
</dt> <dd> <dl> <dt>

(BITS \_ opção de custo ignorar bits de \_ \_ congestionamento do estado de custo de \_ \| \_ \_ \_ roaming bits \| \_ \_ \_ \_ com base no uso do estado \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ de custo de bits de estado OVERCAP limitado do estado de custo OVERCAP de custo de bits restritos estado do custo do bits de limite inferior do estado do custo do bits de limite de bits
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Bits5 \_ 0. h (incluir bits. h)</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Bits5 \_ 0. idl</dt> </dl>                |



 

 





