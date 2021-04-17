---
description: Descreve um serviço de ponto de referência do sistema virtual.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105758329"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>\_Classe Msvm VirtualSystemReferencePointService

Descreve um serviço de ponto de referência do sistema virtual.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemReferencePointService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Msvm \_ VirtualSystemReferencePointService** tem esses métodos.



| Método                                                                                                       | Descrição                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Cria um ponto de referência de um sistema virtual.<br/>            |
| [**DestroyReferencePoint**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Exclui o ponto de referência especificado.<br/>                    |
| [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Exporta o ponto de referência do sistema virtual.<br/>        |
| [**ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Importa os metadados do ponto de referência do sistema virtual.<br/>   |
| [**RemoveAssociatedData**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Remove o log de dados associado ao ponto de referência.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

 




