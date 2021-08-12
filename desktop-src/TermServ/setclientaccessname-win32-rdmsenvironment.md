---
title: Método SetClientAccessName da classe Win32_RDMSEnvironment
description: Atualiza o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) de um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetClientAccessName
- Método SetClientAccessName Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb962a6dd1600ad0cd439f7f34772f69d91b925308e2247e1283575d8f68cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604868"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Método SetClientAccessName da classe Win32 \_ RDMSEnvironment

Atualiza o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) de um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientAccessName* \[ no\]
</dt> <dd>

O nome do novo RR.

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

[**\_RDMSEnvironment Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





