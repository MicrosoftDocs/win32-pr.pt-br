---
title: Método GetClientAccessName da classe Win32_RDMSEnvironment
description: Recupera o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) do ambiente dos serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetClientAccessName
- Método GetClientAccessName Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760132"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Método GetClientAccessName da classe Win32 \_ RDMSEnvironment

Recupera o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) do ambiente dos serviços de gerenciamento de Área de Trabalho Remota (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientAccessName* \[ fora\]
</dt> <dd>

Recebe o nome do RR recuperado.

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

[**\_RDMSEnvironment Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





