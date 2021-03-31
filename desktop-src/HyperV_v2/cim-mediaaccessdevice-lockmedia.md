---
description: Bloqueia e desbloqueia a mídia em um dispositivo de acesso removível.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Método LockMedia da classe CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011911"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a>Método LockMedia da \_ classe MEDIAACCESSDEVICE CIM

Bloqueia e desbloqueia a mídia em um dispositivo de acesso removível.

## <a name="syntax"></a>Sintaxe


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Bloquear* \[ no\]
</dt> <dd>

Se **for true**, bloqueará a mídia. Se **for false**, libera a mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_MEDIAACCESSDEVICE CIM**](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




