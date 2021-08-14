---
title: Método setstringproperty da classe Win32_RDMSDeploymentSettings (CertEnroll. h)
description: Atualiza uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Método setstringproperty Serviços de Área de Trabalho Remota
- Método setstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método setstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1001d5c723642357263a6029c3569eaa861f7dcf3689cc7d06b42e04ef461aa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987496"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método setstringproperty da classe Win32 \_ RDMSDeploymentSettings

Atualiza uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

O alias para a coleção de áreas de trabalho virtuais.

</dd> <dt>

*Valor* \[ do no\]
</dt> <dd>

O novo valor da propriedade.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| Cabeçalho<br/>                   | <dl> <dt>CertEnroll. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





