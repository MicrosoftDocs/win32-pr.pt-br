---
description: Bloqueia ou desbloqueia a mídia.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Método LockMedia da classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d6a3b35b418427a4af8f86dfb162cff7009539d93eab3d87f0c96423a5e951e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130576"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a>Método LockMedia da \_ classe DiskDrive Msvm

Bloqueia ou desbloqueia a mídia.

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
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ DiskDrive**](msvm-diskdrive.md)
</dt> </dl>

 

 




