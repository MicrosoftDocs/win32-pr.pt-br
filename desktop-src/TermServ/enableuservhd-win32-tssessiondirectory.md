---
title: Método EnableUserVhd da classe Win32_TSSessionDirectory
description: Habilita um VHD de perfil de usuário em um servidor RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableUserVhd
- Método EnableUserVhd Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757937"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Método EnableUserVhd da classe Win32 \_ TSSessionDirectory

Habilita um VHD de perfil de usuário em um servidor RDSH.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UvhdShareUrl* \[ no\]
</dt> <dd>

O local do compartilhamento onde todos os VHDs de perfil de usuário são armazenados.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ no\]
</dt> <dd>

A política de roaming para o VHD do perfil de usuário.

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

 

 





