---
title: Método GetConnectionString da Win32_RDMSDeploymentSettings classe
description: Recupera a cadeia de conexão de banco de dados no nível da implantação.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Método GetConnectionString Serviços de Área de Trabalho Remota
- Método GetConnectionString Serviços de Área de Trabalho Remota , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Serviços de Área de Trabalho Remota , método GetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38462e6bceda70638d77699fd5d1ecfea28d3ab1ae39ed0c6fcfbe59deac4ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118849880"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetConnectionString da classe Win32 \_ RDMSDeploymentSettings

Recupera a cadeia de conexão de banco de dados no nível da implantação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConnectionString* \[ out\]
</dt> <dd>

A cadeia de conexão

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Raiz \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





