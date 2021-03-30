---
description: A função WiaAddDevice invoca a interface do usuário do assistente de instalação da câmera e scanner. É equivalente a executar &\# 0034; rundll32.exe sti \_ci.dll adddevice&\# 0034; no prompt de comando.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Função WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647212"
---
# <a name="wiaadddevice-function"></a>Função WiaAddDevice

A função **WiaAddDevice** invoca a interface do usuário do assistente de instalação da câmera e scanner. É equivalente a executar "rundll32.exe STI \_ci.dll adddevice" no prompt de comando.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função deve ser chamada com credenciais de administrador. Ao ser executado sob o controle de conta de usuário (LUA), o processo deve ser elevado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




