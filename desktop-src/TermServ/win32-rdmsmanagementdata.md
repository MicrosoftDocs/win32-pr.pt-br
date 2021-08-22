---
title: Classe Win32_RDMSManagementData
description: Sincroniza dados de publicação para serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSManagementData Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSManagementData classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c6db0223a18c2fa43de8eed38e670aea36c024f1e66509005bb74f0a8f1cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118849277"
---
# <a name="win32_rdmsmanagementdata-class"></a>\_Classe Win32 RDMSManagementData

Sincroniza dados de publicação para serviços de gerenciamento de Área de Trabalho Remota (RDMS).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSManagementData** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSManagementData** tem esses métodos.



| Método                                                                                        | Descrição                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SynchronizeAllPublishingData**](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | Sincroniza todos os dados de publicação para RDMS.<br/>                  |
| [**SynchronizePublishingData**](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | Sincroniza o conjunto especificado de dados de publicação para RDMS.<br/> |



 

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

 

 





