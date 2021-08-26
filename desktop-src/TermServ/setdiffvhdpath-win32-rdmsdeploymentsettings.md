---
title: Método SetDiffVHDPath da classe Win32_RDMSDeploymentSettings
description: Atualiza o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Método SetDiffVHDPath Serviços de Área de Trabalho Remota
- Método SetDiffVHDPath Serviços de Área de Trabalho Remota , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Serviços de Área de Trabalho Remota , método SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d275f848bb29c9cac4930f738a9a123cc6aa3a8e80a77b746f2495d44f68cf96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988036"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetDiffVHDPath da classe Win32 \_ RDMSDeploymentSettings

Atualiza o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DirectoryPath* \[ Em\]
</dt> <dd>

O novo caminho do disco diferencial.

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

 

 





