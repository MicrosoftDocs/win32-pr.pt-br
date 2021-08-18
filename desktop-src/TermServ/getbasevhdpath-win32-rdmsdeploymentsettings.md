---
title: Método GetBaseVHDPath da classe Win32_RDMSDeploymentSettings classe
description: Recupera o caminho base para o diretório no qual os VHDs da coleção de área de trabalho virtual são implantados. | Método GetBaseVHDPath da classe Win32_RDMSDeploymentSettings classe
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- Método GetBaseVHDPath Serviços de Área de Trabalho Remota
- Método GetBaseVHDPath Serviços de Área de Trabalho Remota , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Serviços de Área de Trabalho Remota , método GetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44d2379d498f5e191296a132c30b5fde925c9c323d4f42f1a316ed6cb0a4c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010182"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetBaseVHDPath da classe Win32 \_ RDMSDeploymentSettings

Recupera o caminho base para o diretório no qual os VHDs da coleção de área de trabalho virtual são implantados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Recebe o caminho de implantação do VHD.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\rdms CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





