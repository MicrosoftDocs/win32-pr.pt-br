---
title: Método IRemoteDesktopClientEvents OnKeyCombinationPressed
description: Chamado quando as combinações de teclas especiais são pressionadas na sessão remota.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnKeyCombinationPressed
- Método OnKeyCombinationPressed Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnKeyCombinationPressed
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369432"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a>Método IRemoteDesktopClientEvents:: OnKeyCombinationPressed

Chamado quando as combinações de teclas especiais são pressionadas na sessão remota.

## <a name="syntax"></a>Sintaxe


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*combinação de teclas* \[ no\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





