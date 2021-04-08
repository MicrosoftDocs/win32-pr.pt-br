---
title: Método IMsTscAxEvents OnLeaveFullScreenMode
description: Chamado quando o cliente deixa o modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de teclas de atalho no modo de tela inteira (CTRL + ALT + BREAK).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnLeaveFullScreenMode
- Método OnLeaveFullScreenMode Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnLeaveFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009511"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a>Método IMsTscAxEvents:: OnLeaveFullScreenMode

Chamado quando o cliente deixa o modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).

## <a name="syntax"></a>Sintaxe


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





