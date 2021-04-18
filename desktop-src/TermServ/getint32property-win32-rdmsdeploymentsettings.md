---
title: Método getint32property da classe Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Recupera uma propriedade de número inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Método getint32property Serviços de Área de Trabalho Remota
- Método getint32property Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método getint32property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810986"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método getint32property da classe Win32 \_ RDMSDeploymentSettings

Recupera uma propriedade de número inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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

Um inteiro que recebe o valor recuperado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                                   |
| parâmetro<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





