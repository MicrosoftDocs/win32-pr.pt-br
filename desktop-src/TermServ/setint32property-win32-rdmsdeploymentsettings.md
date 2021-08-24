---
title: Método SetInt32Property da classe Win32_RDMSDeploymentSettings
description: Atualiza uma propriedade de inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Serviços de Área de Trabalho Remota
- Método SetInt32Property Serviços de Área de Trabalho Remota , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Serviços de Área de Trabalho Remota , método SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fa8f9ad7560e4d0eeeb8708feb547da00a8e9804e242ceb94666da211b03a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865376"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetInt32Property da classe Win32 \_ RDMSDeploymentSettings

Atualiza uma propriedade de inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

O alias da coleção de área de trabalho virtual.

</dd> <dt>

*Valor* \[ Em\]
</dt> <dd>

O novo valor da propriedade.

</dd> </dl>

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

 

 





