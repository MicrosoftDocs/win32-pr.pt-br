---
title: Método SetUserAssignment da classe Win32_RDMSVirtualDesktop
description: Atribui uma área de trabalho virtual a um usuário.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserAssignment
- Método SetUserAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método SetUserAssignment
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
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770446"
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

*Nome de usuário* \[ no\]
</dt> <dd>

O nome de usuário do usuário.

</dd> <dt>

*UserDomain* \[ no\]
</dt> <dd>

O nome de domínio do usuário.

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

 

 





