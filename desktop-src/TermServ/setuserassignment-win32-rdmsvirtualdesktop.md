---
title: Método SetUserAssignment da classe Win32_RDMSVirtualDesktop
description: Atribui uma área de trabalho virtual a um usuário.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Método SetUserAssignment Serviços de Área de Trabalho Remota
- Método SetUserAssignment Serviços de Área de Trabalho Remota , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Serviços de Área de Trabalho Remota , método SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38f87209ba8c8ebd82637f72cea2e798844e6081cd000f2161ee21681422e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349407"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método SetUserAssignment da classe Win32 \_ RDMSVirtualDesktop

Atribui uma área de trabalho virtual a um usuário.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UserName* \[ Em\]
</dt> <dd>

O nome de usuário do usuário.

</dd> <dt>

*UserDomain* \[ Em\]
</dt> <dd>

O nome de domínio do usuário.

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

 

 





