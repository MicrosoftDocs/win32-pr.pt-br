---
title: Classe Win32_RdvhManagement
description: Descreve um serviço de gerenciamento de Área de Trabalho Remota host virtual (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RdvhManagement Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RdvhManagement classe, descrita
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea403621aa23cb999bdf2fe692e2d4e053866492608e71346d978cb764ab005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422576"
---
# <a name="win32_rdvhmanagement-class"></a>\_Classe Win32 RdvhManagement

Descreve um serviço de gerenciamento de Área de Trabalho Remota host virtual (RDVH).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RdvhManagement** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RdvhManagement** tem esses métodos.



| Método                                                                                  | Descrição                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Cria o modelo de disco do usuário de tamanho máximo especificado e no local especificado. Todos os discos de usuário criados terão tamanhos máximos correspondentes ao tamanho máximo do modelo.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Inicia uma migração dinâmica de máquina virtual em cenários de VDI<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Copia o local da VM base localmente para o Host RDV Server<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Cria o modelo de disco do usuário de tamanho máximo especificado e no local especificado. Todos os discos de usuário criados terão tamanhos máximos correspondentes ao tamanho máximo do modelo.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Inicia uma migração dinâmica de máquina virtual em cenários de VDI.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Define permissões na VM para o chamador<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Reverte as permissões na VM definida por RdvSetupVMPermissions<br/>                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





