---
description: A associação CIM \_ ChassisInRack representa o &\# 0034;que contém&0034; relação entre um rack e um chassi que ele \# contém.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: CIM_ChassisInRack classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 765b5e36fcb5f2cfe400d9dec9ba86d37cd29af8c756ae8416f7aece803f9052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065206"
---
# <a name="cim_chassisinrack-class"></a>Classe CIM \_ ChassisInRack

A **associação \_ CIM ChassisInRack** representa a relação "que contém" entre um rack e um chassi que ela contém.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ChassisInRack** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ ChassisInRack** tem essas propriedades.

<dl> <dt>

**BottomU**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")
</dt> </dl>

Inteiro que indica o "U" mais baixo ou inferior no qual o chassi está montado. Um "U" é uma unidade de medida padrão para a altura de um rack ou componente montável em rack e é igual a 1,75 polegada ou 4,445 centímetros.

</dd> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Rack CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ Rack CIM**](cim-rack.md) que descreve o rack que contém o chassi.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico. Informações relativas a elementos estacionários no contêiner (por exemplo, "segunda unidade da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade. Essa cadeia de caracteres pode complementar ou ser usada no lugar de inciar o [**objeto Local CIM. \_**](cim-location.md)

Essa propriedade é herdada do [**contêiner CIM. \_**](cim-container.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Chassi CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ Chassi CIM**](cim-chassis.md) que descreve o chassi montado no rack.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ ChassisInRack** é derivada do [**contêiner CIM. \_**](cim-container.md)

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Contêiner \_ CIM**](cim-container.md)
</dt> </dl>

 

