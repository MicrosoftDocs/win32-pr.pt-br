---
description: Método LockMedia da classe Msvm_DVDDrive - bloqueia ou libera a mídia.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Método LockMedia da classe Msvm_DVDDrive dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e86ef975d872f0fd86922f25f9752fda7508a037e293db85245ef6b1384a1570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525316"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>Método LockMedia da classe Msvm \_ DVDDrive

Bloqueia ou libera a mídia.

## <a name="syntax"></a>Sintaxe


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Bloqueio* \[ Em\]
</dt> <dd>

**true** para bloquear a mídia; **false** para liberar a mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ DVDDrive**](msvm-dvddrive.md)
</dt> </dl>

 

 




