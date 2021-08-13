---
description: Representa uma porta switch que envia e recebe quadros de dados.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: CIM_SwitchPort classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e52fc85f0891c5b8d1bc88f39437b4a70c5a172ba9af3ba02b08cc6b45dd6235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647184"
---
# <a name="cim_switchport-class"></a>Classe \_ SWITCHPort CIM

Representa uma porta switch que envia e recebe quadros de dados.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a>Membros

A **classe \_ SwitchPort cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SWITCHPort cim** tem essas propriedades.

<dl> <dt>

**Número_da_porta**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dPort")
</dt> </dl>

O identificador numérico da porta switch.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Protocolo \_ CIMEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

