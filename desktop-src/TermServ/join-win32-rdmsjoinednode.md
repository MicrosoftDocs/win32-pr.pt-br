---
title: Método Join da classe Win32_RDMSJoinedNode
description: Adiciona um nó a serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de junção
- Método Join Serviços de Área de Trabalho Remota, classe Win32_RDMSJoinedNode
- Serviços de Área de Trabalho Remota de classe Win32_RDMSJoinedNode, método Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369364"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Método Join da classe Win32 \_ RDMSJoinedNode

Adiciona um nó a serviços de gerenciamento de Área de Trabalho Remota (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NodeFQDN* \[ no\]
</dt> <dd>

O nome de domínio totalmente qualificado do nó.

</dd> <dt>

*NodeId* \[ no\]
</dt> <dd>

O identificador de segurança (SID) do nó.

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

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





