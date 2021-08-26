---
title: Método RemoveUserAssignment da classe Win32_RDMSVirtualDesktop
description: Remove a atribuição de usuário da área de trabalho virtual.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Método RemoveUserAssignment Serviços de Área de Trabalho Remota
- Método RemoveUserAssignment Serviços de Área de Trabalho Remota , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Serviços de Área de Trabalho Remota , método RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58fa11b22ec089d555fd1e769c71b3fc9d53dbf038ff8b22fb3df559cce59c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988446"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método RemoveUserAssignment da classe Win32 \_ RDMSVirtualDesktop

Remove a atribuição de usuário da área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VMName* \[ Em\]
</dt> <dd>

O nome da máquina virtual da área de trabalho virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

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

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





