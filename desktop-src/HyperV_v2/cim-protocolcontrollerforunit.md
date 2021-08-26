---
description: Representa uma associação entre um controlador de protocolo e uma unidade lógica exposta.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: CIM_ProtocolControllerForUnit classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2722bca49dbac3996295c2937003877321d5c58eb8394b4405d9ce9afce65b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981166"
---
# <a name="cim_protocolcontrollerforunit-class"></a>Classe CIM \_ ProtocolControllerForUnit

Representa uma associação entre um controlador de protocolo e uma unidade lógica exposta.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ProtocolControllerForUnit** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ ProtocolControllerForUnit** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Protocolo \_ CIMController**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

O controlador de protocolo.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

A unidade lógica associada ao controlador de protocolo.

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os direitos de acesso concedidos à unidade lógica por meio do controlador de protocolo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

**Leitura de gravação** (2)


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

**Somente leitura** (3)


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

**Sem acesso** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (5..15999)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor Reservado** (16000..)


</dt> <dd></dd> </dl>

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

[**Protocolo \_ CIMControllerForDevice**](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

