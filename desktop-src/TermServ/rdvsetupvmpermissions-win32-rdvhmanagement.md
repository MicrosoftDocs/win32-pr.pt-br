---
title: Método RdvSetupVMPermissions da classe Win32_RdvhManagement
description: Define as permissões em uma máquina virtual para o usuário atual.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Método RdvSetupVMPermissions Serviços de Área de Trabalho Remota
- Método RdvSetupVMPermissions Serviços de Área de Trabalho Remota , Win32_RdvhManagement classe
- Win32_RdvhManagement classe Serviços de Área de Trabalho Remota , método RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6628e3ac1660c1f0c505e3d5349dd481c7c48b09a77aaedeac1352ecbaf4562
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988806"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Método RdvSetupVMPermissions da classe Win32 \_ RdvhManagement

Define as permissões em uma máquina virtual para o usuário atual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VmName* \[ Em\]
</dt> <dd>

O nome da máquina virtual para definir permissões.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





