---
description: A função WiaAddDevice invoca a interface do usuário do Assistente de Instalação do Scanner e da Câmera. É equivalente a executar &\# 0034;rundll32.exe \_ci.dll AddDevice&\# 0034; no prompt de comando.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Função WiaAddDevice (Wia.h)
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
ms.openlocfilehash: 81dcff3cdca3459126751b12b86f1e11adc2b4fec8926f69211f0508253b64fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965395"
---
# <a name="wiaadddevice-function"></a>Função WiaAddDevice

A **função WiaAddDevice** invoca a interface do usuário do Assistente de Instalação do Scanner e da Câmera. É equivalente a executar "rundll32.execi.dll \_ AddDevice" no prompt de comando.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função deve ser chamada com credenciais de administrador. Ao executar em LUA (Controle de Conta de Usuário), o processo deve ser elevado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




