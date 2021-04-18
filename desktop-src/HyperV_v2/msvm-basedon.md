---
description: Uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Classe Msvm_BasedOn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753474"
---
# <a name="msvm_basedon-class"></a>\_Classe com base em Msvm

Uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior. Por exemplo, ProtectedSpaceExtents são partes de PhysicalExtents, enquanto VolumeSets são montados de um ou mais físicos ou de ProtectedSpaceExtents. Como outro exemplo, o CacheMemory pode ser definido de forma independente e realizado em um Físicoelement ou pode ser baseado em volátil ou NonVolatileStorageExtents.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Membros

A **classe \_ com base em Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ com base em Msvm** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A extensão de armazenamento de nível inferior. Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A extensão de armazenamento de nível superior. Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço final em que, em um armazenamento de nível inferior, a extensão de nível superior termina. Essa propriedade é útil ao mapear extensões não contíguas em um agrupamento de nível superior. Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se houver um pedido para o com base em associações que descrevem como uma extensão de armazenamento de nível superior é montada, a propriedade **OrderIndex** indica isso. Quando um pedido existe, as instâncias com o mesmo valor **dependente** (a mesma extensão de nível superior) devem posicionar valores exclusivos na propriedade **OrderIndex** . O valor mais baixo implica o primeiro membro da coleção de extensões de nível inferior, e os valores crescentes sugerem Membros sucessivos da coleção. Se não houver nenhuma relação ordenada, um valor de zero deverá ser especificado. Um exemplo do uso dessa propriedade é definir uma matriz distribuída RAID-0 de três discos. A matriz de RAID resultante é uma extensão de armazenamento que é dependente das extensões de armazenamento que descrevem cada um dos três discos. A **OrderIndex** de cada associação das extensões de disco para a matriz RAID pode ser especificada como 1, 2 e 3 para indicar a ordem na qual as extensões de disco são usadas para acessar os dados RAID. Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço inicial em que, em armazenamento de nível inferior, começa a extensão de nível superior. Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

