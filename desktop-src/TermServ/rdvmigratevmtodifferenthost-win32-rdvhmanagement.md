---
title: Método RdvMigrateVmToDifferentHost da classe Win32_RdvhManagement
description: Inicia uma migração dinâmica de uma máquina virtual para um host especificado.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvMigrateVmToDifferentHost
- Método RdvMigrateVmToDifferentHost Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvMigrateVmToDifferentHost
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a84171bc6db6a39cff5a2d55ca7e453bf9b963636ea765480fe87b16fd8da92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756238"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a>Método RdvMigrateVmToDifferentHost da classe Win32 \_ RdvhManagement

Inicia uma migração dinâmica de uma máquina virtual para um host especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VmName* \[ no\]
</dt> <dd>

Nome da máquina virtual a ser migrada.

</dd> <dt>

*DestinationHost* \[ no\]
</dt> <dd>

nome do host de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





