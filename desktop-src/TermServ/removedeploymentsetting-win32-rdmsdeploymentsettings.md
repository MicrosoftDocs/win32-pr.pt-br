---
title: Método RemoveDeploymentSetting da classe Win32_RDMSDeploymentSettings
description: Exclui as configurações de implantação para uma coleção de áreas de trabalho virtuais.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveDeploymentSetting
- Método RemoveDeploymentSetting Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método RemoveDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824775"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método RemoveDeploymentSetting da classe Win32 \_ RDMSDeploymentSettings

Exclui as configurações de implantação para uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

O alias da coleção de áreas de trabalho virtuais.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





