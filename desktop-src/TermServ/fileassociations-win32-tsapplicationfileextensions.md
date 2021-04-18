---
title: Método fileassociações da classe Win32_TSApplicationFileExtensions
description: Examina o registro para obter as associações de arquivo atuais para um aplicativo.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Método fileassociationes Serviços de Área de Trabalho Remota
- Método fileassociationes Serviços de Área de Trabalho Remota, classe Win32_TSApplicationFileExtensions
- Classe de Win32_TSApplicationFileExtensions Serviços de Área de Trabalho Remota, método FileAssociations
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
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767729"
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

*AppPath* \[ no\]
</dt> <dd>

Especifica o caminho para o aplicativo.

</dd> <dt>

*Associações* \[ de fora\]
</dt> <dd>

Após a conclusão bem-sucedida, contém as associações de arquivo para este aplicativo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSApplicationFileExtensions Win32**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**\_RDFileAssociation Win32**](win32-rdfileassociation.md)
</dt> </dl>

 

 





