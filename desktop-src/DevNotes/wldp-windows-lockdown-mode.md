---
description: Descreve os modos seguros (S) para um dispositivo Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Enumeração de WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
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
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755273"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>\_Enumeração do \_ modo de bloqueio do Windows WLDP \_

Descreve os modos seguros (S) para um dispositivo Windows. Usado principalmente em [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

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

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_modo de bloqueio do Windows WLDP \_ \_ \_ desbloqueado**
</dt> <dd>

Sala. Usado principalmente para dispositivos Windows sem o modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**\_avaliação do \_ modo de bloqueio do Windows WLDP \_ \_**
</dt> <dd>

Avaliação. Usado principalmente para um dispositivo de avaliação do Windows 10 com o modo S. O modo de avaliação é um caso especial para dispositivos Windows 10 com o modo S: as políticas são impostas, mas não há nenhuma proteção de proversão para a imposição da política.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**\_modo de bloqueio do Windows WLDP \_ \_ \_ bloqueado**
</dt> <dd>

Bloqueadas. Usado principalmente para um dispositivo Windows 10 com o modo S. Um dispositivo bloqueado imporá as políticas de proteção de dispositivo assinadas enviadas com a imagem do sistema operacional do Windows 10 com o modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**\_modo de bloqueio do Windows WLDP \_ \_ \_ Max**
</dt> <dd>

O valor máximo de enumeração.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




