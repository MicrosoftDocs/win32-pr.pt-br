---
title: Método GetJoinedNodeCount da classe Win32_RDMSJoinedNode
description: Obtém o número de servidores que têm as funções especificadas instaladas.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetJoinedNodeCount
- Método GetJoinedNodeCount Serviços de Área de Trabalho Remota, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Serviços de Área de Trabalho Remota, método GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754161"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Método GetJoinedNodeCount da classe Win32 \_ RDMSJoinedNode

Obtém o número de servidores que têm as funções especificadas instaladas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RoleType* \[ no\]
</dt> <dd>

Um campo de bits que especifica os tipos de função.

<dt>

0
</dt> <dd>

Tudo

</dd> <dt>

1
</dt> <dd>

Agente de Conexão de Área de Trabalho Remota (RDCB)

</dd> <dt>

2
</dt> <dd>

Host da Sessão da Área de Trabalho Remota (RDSH)

</dd> <dt>

4
</dt> <dd>

Host de Virtualização de Área de Trabalho Remota (RDVH)

</dd> </dl> </dd> <dt>

*Contagem* \[ de fora\]
</dt> <dd>

Em caso de sucesso, retorna o número de servidores com as funções especificadas instaladas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





