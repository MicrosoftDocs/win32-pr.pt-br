---
description: Contém informações sobre um processador.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Estrutura de PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296746"
---
# <a name="processor_power_information-structure"></a>Estrutura de informações de \_ energia do processador \_

Contém informações sobre um processador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Número**
</dt> <dd>

O número do processador do sistema.

</dd> <dt>

**MaxMhz**
</dt> <dd>

A frequência de relógio máxima especificada do processador do sistema, em megahertz.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

A frequência do relógio do processador, em megahertz. Esse número é a frequência máxima de relógio do processador especificada multiplicada pelo acelerador atual do processador.

</dd> <dt>

**MhzLimit**
</dt> <dd>

O limite da frequência do relógio do processador, em megahertz. Esse número é a frequência máxima de relógio do processador especificada multiplicada pelo limite de aceleração térmica do processador atual.

</dd> <dt>

**MaxIdleState**
</dt> <dd>

O estado ocioso máximo deste processador.

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

O estado ocioso atual deste processador.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que essa definição de estrutura foi acidentalmente omitida de WinNT. h. Esse erro será corrigido no futuro. Enquanto isso, para compilar seu aplicativo, inclua a definição de estrutura contida neste tópico em seu código-fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




