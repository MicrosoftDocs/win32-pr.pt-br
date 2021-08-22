---
description: Contém informações sobre a inatividade do sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Estrutura de SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 665c19a99bffae46cf20af8c5c634e2e9594ecd07d02f003f56d42277ce9a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143299"
---
# <a name="system_power_information-structure"></a>Estrutura de informações de \_ energia do sistema \_

Contém informações sobre a inatividade do sistema.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**MaxIdlenessAllowed**
</dt> <dd>

A ociosidade na qual o sistema é considerado ocioso e o tempo limite ocioso começa a contar, expresso como uma porcentagem. Descartar abaixo desse número faz com que o temporizador seja cancelado.

</dd> <dt>

**Ociosidade**
</dt> <dd>

O nível ocioso atual, expresso como uma porcentagem.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

O tempo restante no temporizador ocioso, em segundos.

</dd> <dt>

**Coolmode**
</dt> <dd>

O modo de resfriamento do sistema atual. Esse membro deve ter um dos valores a seguir.



| Valor                                                                                                                                                                                                                                 | Significado                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Po \_ TZ \_ ativo**</dt> <dt>0</dt> </dl>                    | O sistema está atualmente no modo de resfriamento ativo.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Po \_ \_ \_ Modo inválido de TZ**</dt> <dt>2</dt> </dl> | O sistema não dá suporte à limitação da CPU ou não há zona termal definida no sistema.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Po \_ TZ \_ passivo**</dt> <dt>1</dt> </dl>                 | O sistema está atualmente no modo de resfriamento passivo.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que essa definição de estrutura foi acidentalmente omitida de WinNT. h. Esse erro será corrigido no futuro. Enquanto isso, para compilar seu aplicativo, inclua a definição de estrutura contida neste tópico em seu código-fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




