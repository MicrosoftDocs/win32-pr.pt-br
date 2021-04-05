---
description: Representa uma associação entre um objeto CIM StorageExtent de nível mais alto \_ e um objeto STORAGEEXTENT CIM de nível inferior \_ . Por exemplo, um \_ objeto CIM ProtectedSpaceExtent faz parte de um \_ objeto CIM PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Classe CIM_BasedOn (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827062"
---
# <a name="cim_basedon-class-hyper-v-management"></a>Classe CIM_BasedOn (gerenciamento do Hyper-V)

Representa uma associação entre um objeto **CIM \_ StorageExtent** de nível mais alto e um **objeto \_ StorageExtent CIM** de nível inferior. Por exemplo, um objeto [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) faz parte de um objeto [**CIM \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Membros

A **classe \_ com base em CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ baseded CIM** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

O objeto **CIM \_ StorageExtent** de nível inferior.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

O objeto **CIM \_ StorageExtent** de nível superior.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço que indica onde no armazenamento de nível inferior, o objeto **CIM \_ StorageExtent** de nível superior termina. Essa propriedade é útil ao mapear objetos **CIM \_ StorageExtent** não contíguos em um agrupamento de nível superior.

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um índice que é usado para especificar a ordem das **associações \_ baseadas em CIM** em uma coleção; caso contrário, "0" indicará nenhuma ordem. **CIM \_** As instâncias com base no mesmo valor dependente devem posicionar valores exclusivos na propriedade **OrderIndex** . O valor **OrderIndex** mais baixo especifica o primeiro membro da coleção.

Um exemplo do uso dessa propriedade é definir uma matriz distribuída RAID-0 de 3 discos. A matriz de RAID resultante é uma extensão de armazenamento que é dependente das extensões de armazenamento que descrevem cada um dos três discos. O valor de **OrderIndex** de cada associação de **\_ base CIM** das extensões de disco para a matriz RAID pode ser especificado como 1, 2 e 3 para indicar a ordem na qual as extensões de disco são usadas para acessar os dados RAID.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço que indica onde no armazenamento de nível inferior, o objeto **\_ StorageExtent de CIM** de nível superior começa.

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

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

