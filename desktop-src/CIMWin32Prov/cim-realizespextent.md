---
description: A associação CIM RealizesPExtent representa a relação na qual as extensão \_ físicas são realizadas em uma mídia física. Além disso, o endereço inicial da extensão física na mídia física é especificado.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: CIM_RealizesPExtent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 697ca0386d03ade55895f63cab67b3144bf50b3d0ffea2928633384e4d1f502a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920836"
---
# <a name="cim_realizespextent-class"></a>Classe CIM \_ RealizesPExtent

A **associação CIM \_ RealizesPExtent** representa a relação na qual as extensão físicas são realizadas em uma mídia física. Além disso, o endereço inicial da extensão física na mídia física é especificado.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ RealizesPExtent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ RealizesPExtent** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecessor"), [**Máx.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**Cim \_ PhysicalMedia**](cim-physicalmedia.md) que descreve a mídia física na qual a extensão é realizada.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ PhysicalExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um [**Cim \_ PhysicalExtent**](cim-physicalextent.md) que descreve a extensão física localizada na mídia.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço inicial na mídia física em que a extensão física começa. O endereço final da extensão física é determinado usando as **propriedades NumberOfBlocks** e **BlockSize** do [**objeto \_ PhysicalExtent cim.**](cim-physicalextent.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ RealizesPExtent** é derivada de [**CIM \_ Realizes**](cim-realizes.md).

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

[**Cim \_ Realiza**](cim-realizes.md)
</dt> </dl>

 

