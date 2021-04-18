---
title: Método Unjoin da classe Win32_RDMSJoinedNode
description: Remove um nó de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Unjoin
- Método Unjoin Serviços de Área de Trabalho Remota, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Serviços de Área de Trabalho Remota, método Unjoin
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
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810427"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Método Unjoin da classe Win32 \_ RDMSJoinedNode

Remove um nó de serviços de gerenciamento de Área de Trabalho Remota (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





