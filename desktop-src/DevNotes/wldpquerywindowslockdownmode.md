---
description: Recupera a versão atual Windows modo seguro. Windows pode estar no modo bloqueado, no modo normal desbloqueado ou no modo de avaliação.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Função WldpQueryWindowsLockdownMode (Wldp.h)
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
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911286"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Função WldpQueryWindowsLockdownMode

Recupera a versão atual Windows modo seguro. Windows pode estar no modo bloqueado, no modo normal desbloqueado ou no modo de avaliação.

## <a name="syntax"></a>Sintaxe


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lockdownMode* \[ out\]
</dt> <dd>

Em caso de êxito, retorna um MODO DE BLOQUEIO DO [**\_ WINDOWS \_ \_ PWLDP**](wldp-windows-lockdown-mode.md) que indica o modo de segurança para o dispositivo Windows 10 atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retornará **S \_ OK se** for bem-sucedido ou um código de falha, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




