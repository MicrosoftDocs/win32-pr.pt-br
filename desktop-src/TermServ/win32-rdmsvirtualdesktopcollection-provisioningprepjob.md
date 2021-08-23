---
title: Método ProvisioningPrepJob da classe Win32_RDMSVirtualDesktopCollection
description: Cria um trabalho de provisionamento de área de trabalho virtual.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningPrepJob
- Método ProvisioningPrepJob Serviços de Área de Trabalho Remota, interface Win32_RDMSVirtualDesktopCollection
- Serviços de Área de Trabalho Remota de interface Win32_RDMSVirtualDesktopCollection, método ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2dab9dcbd606dd32857f0d2dc4b2de3d8516e2b2da10e804fa36254679c1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422836"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningPrepJob da classe Win32 \_ RDMSVirtualDesktopCollection

Cria um trabalho de provisionamento de área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CollectionAlias* \[ no\]
</dt> <dd>

O alias da coleção que hospeda a área de trabalho virtual.

</dd> <dt>

*VMHostName* \[ no\]
</dt> <dd>

O nome do host da máquina virtual.

</dd> <dt>

*VMName* \[ no\]
</dt> <dd>

O nome da máquina virtual.

</dd> <dt>

*ExportToLocation* \[ no\]
</dt> <dd>

O caminho completo o local para exportar o trabalho de provisionamento.

</dd> <dt>

*bSysPrep* \[ no\]
</dt> <dd>

Indica se o trabalho de provisionamento representa uma implantação do Sysprep.

</dd> <dt>

*MachineName* \[ no\]
</dt> <dd>

O nome do computador que hospeda a máquina virtual.

</dd> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

O nome de usuário do administrador da máquina virtual.

</dd> <dt>

*Senha* \[ do no\]
</dt> <dd>

A senha do administrador da máquina virtual.

</dd> <dt>

*JobGuid* \[ fora\]
</dt> <dd>

O **GUID** que identifica exclusivamente o trabalho de provisionamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





