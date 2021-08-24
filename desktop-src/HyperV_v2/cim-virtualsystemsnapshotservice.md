---
description: Representa um serviço que pode criar, aplicar e excluir instantâneos de sistemas virtuais.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: Classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5546c7381eb0830d820af20d7efa03e5d7441a712b872a3ae2167b3e441354d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682686"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a>\_Classe CIM VirtualSystemSnapshotService

Representa um serviço que pode criar, aplicar e excluir instantâneos de sistemas virtuais.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **CIM \_ VirtualSystemSnapshotService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **CIM \_ VirtualSystemSnapshotService** tem esses métodos.



| Método                                                                      | Descrição                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](cim-virtualsystemsnapshotservice-applysnapshot.md)     | Aplica um instantâneo do sistema virtual ao sistema virtual para o sistema virtual de origem.<br/> |
| [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)   | Cria um instantâneo de um sistema virtual.<br/>                                               |
| [**DestroySnapshot**](cim-virtualsystemsnapshotservice-destroysnapshot.md) | Exclui um instantâneo do sistema virtual.<br/>                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

 




