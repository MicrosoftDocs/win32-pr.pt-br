---
description: Serviço para criar, destruir e exportar a coleção de instantâneos de sistemas virtuais.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756929"
---
# <a name="msvm_collectionsnapshotservice-class"></a>\_Classe Msvm CollectionSnapshotService

Serviço para criar, destruir e exportar a coleção de instantâneos de sistemas virtuais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CollectionSnapshotService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Msvm \_ CollectionSnapshotService** tem esses métodos.



| Método                                                                                    | Descrição                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)                     | Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.<br/>                                                                                                                                        |
| [**ConvertToReferencePoint**](msvm-collectionsnapshotservice-converttoreferencepoint.md) | Converta um instantâneo de coleção existente em uma coleção de pontos de referência. A coleção de instantâneos é excluída como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.<br/>                      |
| [**CreateSnapshot**](msvm-collectionsnapshotservice-createsnapshot.md)                   | Cria um instantâneo de uma coleção de sistemas virtuais.<br/>                                                                                                                                                                 |
| [**DestroySnapshot**](msvm-collectionsnapshotservice-destroysnapshot.md)                 | Destruir um instantâneo existente da coleção de sistemas virtuais. Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.<br/>                                                   |
| [**ExportSnapshot**](msvm-collectionsnapshotservice-exportsnapshot.md)                   | Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo. A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.<br/> |



 

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

 

 




