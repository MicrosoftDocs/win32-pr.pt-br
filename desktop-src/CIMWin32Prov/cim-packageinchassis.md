---
description: A associação Cim PackageInChassis representa a relação na qual um chassi pode conter outros pacotes, como \_ outros chassis e cartões.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: CIM_PackageInChassis classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dec66ed5ee930db9bff7917e942de44bdc9582ec130a987e83cbb9d633523cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921296"
---
# <a name="cim_packageinchassis-class"></a>Classe CIM \_ PackageInChassis

A **associação \_ Cim PackageInChassis** representa a relação na qual um chassi pode conter outros pacotes, como outros chassis e cartões.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a>Membros

A **classe \_ CIM PackageInChassis** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CIM PackageInChassis** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Chassi CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ chassi CIM que**](cim-chassis.md) descreve o chassi que contém outros pacotes físicos.

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

Tipo de dados: **Cim \_ PhysicalPackage**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ PhysicalPackage cim**](cim-physicalpackage.md) que descreve o pacote físico contido no chassi.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ Cim PackageInChassis** é derivada do [**contêiner CIM \_**](cim-container.md).

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

 

