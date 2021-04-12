---
title: Método RdvSetupVMPermissions da classe Win32_RdvhManagement
description: Define as permissões em uma máquina virtual para o usuário atual.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvSetupVMPermissions
- Método RdvSetupVMPermissions Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvSetupVMPermissions
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
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455145"
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

*VmName* \[ no\]
</dt> <dd>

O nome da máquina virtual para a qual definir permissões.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RdvhManagement Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





