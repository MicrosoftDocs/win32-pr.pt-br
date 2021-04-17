---
title: Método GetVirtualDesktopAssignedToUser da classe Win32_RDMSVirtualDesktop
description: Recupera a área de trabalho virtual que é atribuída ao usuário especificado.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetVirtualDesktopAssignedToUser
- Método GetVirtualDesktopAssignedToUser Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768554"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopAssignedToUser da classe Win32 \_ RDMSVirtualDesktop

Recupera a área de trabalho virtual que é atribuída ao usuário especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CollectionAlias* \[ no\]
</dt> <dd>

O alias da coleção de áreas de trabalho virtuais que contém a área de trabalho virtual.

</dd> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

O nome de usuário do usuário.

</dd> <dt>

*UserDomain* \[ no\]
</dt> <dd>

O nome de domínio do usuário.

</dd> <dt>

*VMName* \[ fora\]
</dt> <dd>

Recebe o nome da máquina virtual da área de trabalho virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

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

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





