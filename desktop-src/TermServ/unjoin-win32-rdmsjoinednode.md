---
title: Método unjoin da Win32_RDMSJoinedNode classe
description: Remove um nó do RDMS (Área de Trabalho Remota Management Services).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Método unjoin Serviços de Área de Trabalho Remota
- Método unjoin Serviços de Área de Trabalho Remota , Win32_RDMSJoinedNode classe
- Win32_RDMSJoinedNode classe Serviços de Área de Trabalho Remota , método Unjoin
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d2fae16ecb31326ae16bc08efd1fbc56ae2585140d63ce360783226101d4a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424096"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Método unjoin da classe \_ Win32 RDMSJoinedNode

Remove um nó do RDMS (Área de Trabalho Remota Management Services).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





