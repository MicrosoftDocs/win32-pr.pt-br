---
description: Uma associação que descreve como as extensão de armazenamento podem ser montadas de extensão de nível inferior.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn classe
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
ms.openlocfilehash: f3f8138fcc06d5e2d100f38b0333dcbfc5e76c61366da686b313a70d40ffa120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790246"
---
# <a name="msvm_basedon-class"></a>Classe Msvm \_ BasedOn

Uma associação que descreve como as extensão de armazenamento podem ser montadas de extensão de nível inferior. Por exemplo, ProtectedSpaceExtents são partes de PhysicalExtents, enquanto VolumeSets são montados de um ou mais Physical ou ProtectedSpaceExtents. Como outro exemplo, CacheMemory pode ser definido independentemente e realizado em um PhysicalElement ou pode ser baseado em Volatile ou NonVolatileStorageExtents.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ BasedOn** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ BasedOn** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A extensão de armazenamento de nível inferior. Essa propriedade é herdada de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A extensão de armazenamento de nível superior. Essa propriedade é herdada de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço final em que, no armazenamento de nível inferior, a extensão de nível mais alto termina. Essa propriedade é útil ao mapear as extensão não contíguas para um grupo de nível mais alto. Essa propriedade é herdada de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se houver uma ordem para o com base em associações que descrevem como uma extensão de armazenamento de nível superior é montada, a propriedade **OrderIndex** indica isso. Quando existe uma ordem, as  instâncias com o mesmo valor Dependente (a mesma extensão de nível superior) devem colocar valores exclusivos na **propriedade OrderIndex.** O valor mais baixo implica o primeiro membro da coleção de extensão de nível inferior e o aumento de valores implica membros sucessivos da coleção. Se não houver nenhuma relação ordenada, um valor de zero deverá ser especificado. Um exemplo do uso dessa propriedade é definir uma matriz raid-0 de três discos. A matriz RAID resultante é uma extensão de armazenamento que depende das extensão de armazenamento que descrevem cada um dos três discos. O **OrderIndex de** cada associação das extensão de disco para a matriz RAID pode ser especificado como 1, 2 e 3 para indicar a ordem na qual as extensão de disco são usadas para acessar os dados RAID. Essa propriedade é herdada de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço inicial em que, no armazenamento de nível inferior, a extensão de nível mais alto começa. Essa propriedade é herdada de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

