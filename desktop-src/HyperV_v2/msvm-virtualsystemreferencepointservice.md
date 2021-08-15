---
description: Descreve um serviço de ponto de referência do sistema virtual.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService classe
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
ms.openlocfilehash: f33ac35e9848b913978ef6fab91f60823e5c40e9a2bb652236b2ab902e4ea435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340156"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>Classe Msvm \_ VirtualSystemReferencePointService

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

A **classe \_ VirtualSystemReferencePointService do Msvm** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe \_ VirtualSystemReferencePointService do Msvm** tem esses métodos.



| Método                                                                                                       | Descrição                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Cria um ponto de referência de um sistema virtual.<br/>            |
| [**DestroyReferencePoint**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Exclui o ponto de referência especificado.<br/>                    |
| [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Exporta o ponto de referência do sistema virtual.<br/>        |
| [**ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Importa metadados de ponto de referência do sistema virtual.<br/>   |
| [**RemoveAssociatedData**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Remove o log de dados associado ao ponto de referência.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ CIM**](cim-service.md)
</dt> </dl>

 

 




