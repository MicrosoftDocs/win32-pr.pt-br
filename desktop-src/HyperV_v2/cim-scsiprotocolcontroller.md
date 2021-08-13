---
description: Representa um controlador de protocolo que gerencia uma interface SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: CIM_SCSIProtocolController classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f7e3db8cb1d0aa97446d503aff876c0270ddb16e5908b3b1c53c899c7617a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647671"
---
# <a name="cim_scsiprotocolcontroller-class"></a>Classe CIM \_ SCSIProtocolController

Representa um controlador de protocolo que gerencia uma interface SCSI.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ SCSIProtocolController** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ SCSIProtocolController** tem essas propriedades.

<dl> <dt>

**Nameformat**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Nome**", "**CIM \_ SCSIProtocolController**.**OtherNameFormat**")
</dt> </dl>

O formato da **propriedade Name** do **CIM \_ SCSIProtocolController.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

**Fc Port WWN** (2)


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

**Nome iSCSI** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Nome**", "**CIM \_ SCSIProtocolController**.**NameFormat**")
</dt> </dl>

Uma descrição da **propriedade NameFormat** **quando NameFormat** é definido como "1" (outro).

</dd> </dl>

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

[**Protocolo \_ CIMController**](cim-protocolcontroller.md)
</dt> </dl>

 

