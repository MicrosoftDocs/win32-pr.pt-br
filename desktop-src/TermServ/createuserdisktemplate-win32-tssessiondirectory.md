---
title: Método CreateUserDiskTemplate da classe Win32_TSSessionDirectory
description: Cria um modelo de disco de usuário.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Método CreateUserDiskTemplate Serviços de Área de Trabalho Remota
- Método CreateUserDiskTemplate Serviços de Área de Trabalho Remota , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Serviços de Área de Trabalho Remota , método CreateUserDiskTemplate
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
ms.openlocfilehash: cdc16d293f901efb6fc684d03ec7b47aa7496120c462a32414c747d15c02810a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010226"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Método CreateUserDiskTemplate da classe \_ Win32 TSSessionDirectory

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

*UserDisksStorageUrl* \[ Em\]
</dt> <dd>

O local do compartilhamento em que todos os discos de usuário são armazenados.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ Em\]
</dt> <dd>

O tamanho máximo em gigabytes, para todos os discos de usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





