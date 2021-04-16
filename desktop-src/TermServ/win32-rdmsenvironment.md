---
title: Classe Win32_RDMSEnvironment
description: Gerencia um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSEnvironment Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSEnvironment classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754162"
---
# <a name="win32_rdmsenvironment-class"></a>\_Classe Win32 RDMSEnvironment

Gerencia um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSEnvironment** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSEnvironment** tem esses métodos.



| Método                                                                   | Descrição                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetActiveServer**](getactiveserver-win32-rdmsenvironment.md)         | Recupera o FQDN (nome de domínio totalmente qualificado) do ambiente de RDMS.<br/>                 |
| [**GetClientAccessName**](getclientaccessname-win32-rdmsenvironment.md) | Recupera o nome do registro de recurso (DNS) do sistema de nome de domínio (RR) do ambiente de RDMS.<br/> |
| [**SetActiveServer**](setactiveserver-win32-rdmsenvironment.md)         | Define o FQDN do ambiente de RDMS para o nó atual.<br/>                                |
| [**SetClientAccessName**](setclientaccessname-win32-rdmsenvironment.md) | Atualiza o nome do RR DNS do ambiente de RDMS.<br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

 





