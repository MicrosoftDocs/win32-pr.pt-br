---
title: Método RemoveDesktopAssignment da classe Win32_RDMSDesktopAssignment
description: Remove uma atribuição de desktop.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveDesktopAssignment
- Método RemoveDesktopAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSDesktopAssignment
- Classe Win32_RDMSDesktopAssignment Serviços de Área de Trabalho Remota, método RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788024"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Método RemoveDesktopAssignment da classe Win32 \_ RDMSDesktopAssignment

Remove uma atribuição de desktop

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CollectionAlias* \[ no\]
</dt> <dd>

O alias da coleção.

</dd> <dt>

*Área de trabalho* \[ no\]
</dt> <dd>

O nome da área de trabalho.

</dd> <dt>

*UserDomain* \[ no\]
</dt> <dd>

O nome de domínio da conta de usuário.

</dd> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

O nome da conta de usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSDesktopAssignment Win32**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





