---
description: Define os parâmetros do recurso compartilhado.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Método SetShareInfo da classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755433"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Método SetShareInfo da classe Win32 \_ ClusterShare

Define os parâmetros do recurso compartilhado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaximumAllowed* \[ em, opcional\]
</dt> <dd>

Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.

</dd> <dt>

*Descrição* \[ do em, opcional\]
</dt> <dd>

Descreve o recurso que está sendo compartilhado.

</dd> <dt>

*Acesso* \[ ao em, opcional\]
</dt> <dd>

Descritor de segurança para permissões de nível de usuário. Um descritor de segurança contém informações sobre a permissão, o proprietário e os recursos de acesso do recurso. Para obter mais informações, consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ClusterShare Win32**](win32-clustershare.md)
</dt> </dl>

 

