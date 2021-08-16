---
description: Representa um serviço que controla a migração de sistemas virtuais entre sistemas host. Essa classe também verifica se uma migração pendente provavelmente terá êxito.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44b034c5b91eb024bdbcde0b0d835ba12f0367bedc6dbd9c5c2d52dca1029f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068536"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>Classe CIM \_ VirtualSystemMigrationService

Representa um serviço que controla a migração de sistemas virtuais entre sistemas host. Essa classe também verifica se uma migração pendente provavelmente terá êxito.

## <a name="syntax"></a>Sintaxe

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A **classe CIM \_ VirtualSystemMigrationService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe CIM \_ VirtualSystemMigrationService** tem esses métodos.



| Método                                                                                                                     | Descrição                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Verifica se uma migração de sistema virtual pendente para um host provavelmente terá êxito.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Verifica se uma migração de sistema virtual pendente para um sistema provavelmente terá êxito.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Migra um sistema virtual para um host de destino.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Migra um sistema virtual para o sistema de destino.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ CIM**](cim-service.md)
</dt> </dl>

 

 




