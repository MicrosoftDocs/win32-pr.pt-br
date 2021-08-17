---
title: Método GetUserAssignment da classe Win32_RDMSVirtualDesktop
description: Recupera o nome de usuário e o domínio que é atribuído à área de trabalho virtual.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetUserAssignment
- Método GetUserAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff3d63179ec68c38ada5738390979e4844ff2950f91decf82245a6b164dbab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059554"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetUserAssignment da classe Win32 \_ RDMSVirtualDesktop

Recupera o nome de usuário e o domínio que é atribuído à área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome de usuário* \[ fora\]
</dt> <dd>

Recebe o nome de usuário.

</dd> <dt>

*UserDomain* \[ fora\]
</dt> <dd>

Recebe o nome de domínio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





