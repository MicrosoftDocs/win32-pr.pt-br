---
title: Método getstringproperty da classe Win32_RDMSDeploymentSettings
description: Recupera uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369450"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método getstringproperty da classe Win32 \_ RDMSDeploymentSettings

Recupera uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

O alias para a coleção de áreas de trabalho virtuais.

</dd> <dt>

*Valor* \[ do fora\]
</dt> <dd>

Uma cadeia de caracteres que recebe o valor recuperado.

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

 

 





