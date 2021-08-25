---
description: Descreve os modos de segurança (modos S) para um Windows dispositivo.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP_WINDOWS_LOCKDOWN_MODE enumeração (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911336"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>Enumeração WLDP \_ DO MODO DE BLOQUEIO \_ DO WINDOWS \_

Descreve os modos de segurança (modos S) para um Windows dispositivo. Usado principalmente no [**WldpQueryWindowsLockdownMode.**](wldpquerywindowslockdownmode.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**MODO DE BLOQUEIO DO WINDOWS WLDP \_ \_ \_ \_ DESBLOQUEADO**
</dt> <dd>

Desbloqueado. Usado principalmente para Windows dispositivos sem o modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**AVALIAÇÃO DO MODO \_ DE BLOQUEIO DO WINDOWS WLDP \_ \_ \_**
</dt> <dd>

Julgamento. Usado principalmente para um Windows 10 de avaliação com o modo S. O modo de avaliação é um caso especial para Windows 10 dispositivos com o modo S: as políticas são impostas, mas não há proteção anti-replicação para a imposição da política.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**MODO DE BLOQUEIO DO WINDOWS WLDP \_ \_ \_ \_ BLOQUEADO**
</dt> <dd>

Bloqueadas. Usado principalmente para um Windows 10 com o modo S. Um dispositivo bloqueado imporá as políticas assinadas do Device Guard fornecidas com a imagem Windows 10 do sistema operacional com o modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**MODO DE BLOQUEIO MÁXIMO DO WINDOWS WLDP \_ \_ \_ \_**
</dt> <dd>

O valor máximo de enumeração.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wldp.h</dt> </dl> |



 

 




