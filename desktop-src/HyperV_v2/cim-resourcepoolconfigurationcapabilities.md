---
description: Gerencia os recursos da \_ instância ResourcePoolConfigurationService do CIM para um \_ objeto RESOURCEPOOL do CIM.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: Classe CIM_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782365"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a>\_Classe CIM ResourcePoolConfigurationCapabilities

Gerencia os recursos da instância [**\_ ResourcePoolConfigurationService do CIM**](cim-resourcepoolconfigurationservice.md) para um objeto [**\_ ResourcePool do CIM**](cim-resourcepool.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ResourcePoolConfigurationCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ResourcePoolConfigurationCapabilities** tem essas propriedades.

<dl> <dt>

**AsynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os métodos do serviço de configuração que têm suporte para operações assíncronas.

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

**CreateResourcePool tem suporte** (2)


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

**CreateChild ResourcePool tem suporte** (3)


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

**DeleteResourcePool tem suporte** (4)


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

**AddResourcesToResourcePool tem suporte** (5)


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

**RemoveResourcesFromResourcePool tem suporte** (6)


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

**ChangeParentResourcePool tem suporte** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os métodos do serviço de configuração que têm suporte para operações síncronas.

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

**CreateResourcePool tem suporte** (2)


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

**CreateChild ResourcePool tem suporte** (3)


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

**DeleteResourcePool tem suporte** (4)


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

**AddResourcesToResourcePool tem suporte** (5)


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

**RemoveResourcesFromResourcePool tem suporte** (6)


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

**CIM \_ ChangeParentResourcePool tem suporte** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Recursos de CIM \_**](cim-capabilities.md)
</dt> </dl>

 

 




