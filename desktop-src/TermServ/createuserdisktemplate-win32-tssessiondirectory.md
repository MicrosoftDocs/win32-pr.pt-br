---
title: Método CreateUserDiskTemplate da classe Win32_TSSessionDirectory
description: Cria um modelo de disco de usuário.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateUserDiskTemplate
- Método CreateUserDiskTemplate Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085272"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Método CreateUserDiskTemplate da classe Win32 \_ TSSessionDirectory

Cria um modelo de disco de usuário.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UserDisksStorageUrl* \[ no\]
</dt> <dd>

O local do compartilhamento onde todos os discos de usuário são armazenados.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ no\]
</dt> <dd>

O tamanho máximo em gigabytes, para todos os discos de usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





