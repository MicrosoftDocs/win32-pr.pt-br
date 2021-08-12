---
title: Método join da classe Win32_RDMSJoinedNode classe
description: Adiciona um nó ao Área de Trabalho Remota Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Método join Serviços de Área de Trabalho Remota
- Método join Serviços de Área de Trabalho Remota classe , Win32_RDMSJoinedNode de junção
- Win32_RDMSJoinedNode classe Serviços de Área de Trabalho Remota , método Join
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
ms.openlocfilehash: 204d83988f9a57d9fe0edf8daa6dc580676fc7395f98edcbece49674c0041aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605419"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Método join da classe Win32 \_ RDMSJoinedNode

Adiciona um nó ao Área de Trabalho Remota Management Services (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NodeFQDN* \[ Em\]
</dt> <dd>

O nome de domínio totalmente qualificado do nó.

</dd> <dt>

*NodeSID* \[ Em\]
</dt> <dd>

O SID (identificador de segurança) do nó.

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

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





