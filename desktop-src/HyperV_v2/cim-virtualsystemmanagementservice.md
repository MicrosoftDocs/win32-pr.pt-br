---
description: Representa um serviço que gerencia sistemas virtuais.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: Classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768512"
---
# <a name="cim_virtualsystemmanagementservice-class"></a>\_Classe CIM VirtualSystemManagementService

Representa um serviço que gerencia sistemas virtuais.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **CIM \_ VirtualSystemManagementService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **CIM \_ VirtualSystemManagementService** tem esses métodos.



| Método                                                                                      | Descrição                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResourceSettings**](cim-virtualsystemmanagementservice-addresourcesettings.md)       | Adiciona recursos a uma configuração de sistema virtual.<br/>                          |
| [**DefineSystem**](cim-virtualsystemmanagementservice-definesystem.md)                     | Define um sistema virtual.<br/>                                                  |
| [**DestroySystem**](cim-virtualsystemmanagementservice-destroysystem.md)                   | Exclui um sistema virtual.<br/>                                                  |
| [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | Modifica as configurações de recurso virtual para uma configuração de sistema virtual.<br/> |
| [**ModifySystemSettings**](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | Modifica as configurações do sistema virtual.<br/>                                          |
| [**RemoveResourceSettings**](cim-virtualsystemmanagementservice-removeresourcesettings.md) | Remove as configurações de recursos virtuais de uma configuração de sistema virtual.<br/>     |



 

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

 

 




