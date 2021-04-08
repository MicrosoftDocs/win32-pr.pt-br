---
description: A \_ classe WMI de associação AllocatedResource do Win32 relaciona um dispositivo lógico a um recurso do sistema. Essa classe é usada para descobrir quais recursos, como IRQs ou canais DMA, estão em uso por um dispositivo específico.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Classe Win32_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920528"
---
# <a name="win32_allocatedresource-class"></a>\_Classe Win32 AllocatedResource

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ AllocatedResource do Win32** relaciona um dispositivo lógico a um recurso do sistema. Essa classe é usada para descobrir quais recursos, como IRQs ou canais DMA, estão em uso por um dispositivo específico.

Essa classe está obsoleta. No lugar dessa classe, você deve usar as propriedades na classe [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md) .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ AllocatedResource** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ AllocatedResource** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SystemResource**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ SystemResource")
</dt> </dl>

Um [**\_ SystemResource CIM**](cim-systemresource.md) que descreve as propriedades de um recurso do sistema disponível para o dispositivo lógico.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico que está usando os recursos do sistema atribuídos a ele.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ AllocatedResource** é derivada da [**\_ dependência CIM**](cim-dependency.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

