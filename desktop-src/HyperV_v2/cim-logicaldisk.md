---
description: Representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo discos DeviceID (chave).
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Classe CIM_LogicalDisk (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0fccc6600e0eb5f04fd7d00360402ad85a94746e55781acbd6b1a35c7f9b94fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812101"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a>Classe CIM_LogicalDisk (gerenciamento do Hyper-V)

Representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo **DeviceID** (chave) do disco. por exemplo, em um ambiente Windows, o campo **deviceid** contém uma letra da unidade; em um ambiente UNIX, ele contém o caminho de acesso; e em um ambiente do NetWare, ele contém o nome do volume.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a>Membros

A classe do **\_ LogicalDisk CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ LogicalDisk** tem essas propriedades.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Indica se o dispositivo lógico usa o formato de nome do sistema operacional.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Nome do dispositivo do so** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")
</dt> </dl>

Indica se o dispositivo lógico tem o mesmo namespace que o sistema operacional.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Namespace de dispositivo do so** (8)


</dt> <dd></dd> </dl>

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

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> </dl>

 

