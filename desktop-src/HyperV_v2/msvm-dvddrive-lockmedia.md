---
description: Bloqueia ou libera a mídia.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Método LockMedia da classe Msvm_DVDDrive
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
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091893"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>Método LockMedia da \_ classe DVDDrive Msvm

Bloqueia ou libera a mídia.

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

## <a name="return-value"></a>Retornar valor

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

[**Msvm \_ DVDDrive**](msvm-dvddrive.md)
</dt> </dl>

 

 




