---
description: Recupera o modo de segurança atual do Windows. O Windows pode estar no modo bloqueado, no modo normal desbloqueado ou no modo de avaliação.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Função WldpQueryWindowsLockdownMode (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164119"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Função WldpQueryWindowsLockdownMode

Recupera o modo de segurança atual do Windows. O Windows pode estar no modo bloqueado, no modo normal desbloqueado ou no modo de avaliação.

## <a name="syntax"></a>Sintaxe


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lockdownmode* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna um [**\_ modo de \_ bloqueio \_ do Windows PWLDP**](wldp-windows-lockdown-mode.md) que indica o modo de segurança para o dispositivo atual do Windows 10.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




