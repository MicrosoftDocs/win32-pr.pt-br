---
title: Método FileAssociations da classe Win32_TSApplicationFileExtensions dados
description: Examina o registro para obter as associações de arquivo atuais para um aplicativo.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Método FileAssociations Serviços de Área de Trabalho Remota
- Método FileAssociations Serviços de Área de Trabalho Remota , Win32_TSApplicationFileExtensions classe
- Win32_TSApplicationFileExtensions classe Serviços de Área de Trabalho Remota , método FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45548d055d6adc90ac55e26b646abab80470297847d5daa898e63b29769dc4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737506"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Método FileAssociations da classe Win32 \_ TSApplicationFileExtensions

Examina o registro para obter as associações de arquivo atuais para um aplicativo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppPath* \[ Em\]
</dt> <dd>

Especifica o caminho para o aplicativo.

</dd> <dt>

*FileAssociations* \[ out\]
</dt> <dd>

Após a conclusão bem-sucedida, contém as associações de arquivo para este aplicativo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**Win32 \_ RDFileAssociation**](win32-rdfileassociation.md)
</dt> </dl>

 

 





