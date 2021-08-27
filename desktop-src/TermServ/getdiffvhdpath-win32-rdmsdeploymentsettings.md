---
title: Método GetDiffVHDPath da classe Win32_RDMSDeploymentSettings
description: Recupera o caminho do diretório no qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Método GetDiffVHDPath Serviços de Área de Trabalho Remota
- Método GetDiffVHDPath Serviços de Área de Trabalho Remota , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Serviços de Área de Trabalho Remota , método GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad8783d20737c98dcccf769924ea1544c21dec8ffa3ff340aa285be163b8925b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099536"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetDiffVHDPath da classe Win32 \_ RDMSDeploymentSettings

Recupera o caminho do diretório no qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Recebe o novo caminho de disco diferencial.

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

 

 





