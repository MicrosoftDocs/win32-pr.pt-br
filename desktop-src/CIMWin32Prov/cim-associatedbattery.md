---
description: A dependência do CIM \_ AssociatedBattery associa uma bateria a um dispositivo lógico. Use essa associação para modelar baterias individuais que compõem uma fonte de alimentação ininterrupta (UPS).
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164110"
---
# <a name="cim_associatedbattery-class"></a>\_Classe CIM AssociatedBattery

A dependência do **CIM \_ AssociatedBattery** associa uma bateria a um dispositivo lógico. Use essa associação para modelar baterias individuais que compõem uma fonte de alimentação ininterrupta (UPS).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ AssociatedBattery** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ AssociatedBattery** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ bateria CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Uma [**\_ bateria CIM**](cim-battery.md) que descreve a bateria.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que contém o dispositivo lógico que precisa ou está associado à bateria.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ AssociatedBattery** é derivada da [**\_ dependência CIM**](cim-dependency.md).

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas de **CIM \_ AssociatedBattery**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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
</dt> </dl>

 

