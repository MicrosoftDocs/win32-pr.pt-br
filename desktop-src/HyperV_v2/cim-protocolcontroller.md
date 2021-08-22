---
description: Representa um grupo de controladores que controlam a operação e a função de dispositivos que iniciam protocolos.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: Classe CIM_ProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7dcd0f0ca1891914e2c4fc3fedbc0012d930dbaec99926f9db8e013435367f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148500"
---
# <a name="cim_protocolcontroller-class"></a>\_Classe CIM ProtocolController

Representa um grupo de controladores que controlam a operação e a função de dispositivos que iniciam protocolos.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ProtocolController** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ProtocolController** tem essas propriedades.

<dl> <dt>

**MaxUnitsControlled**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número máximo de unidades que podem ser controladas pelo ou acessadas por meio do controlador de protocolo.

</dd> </dl>

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




