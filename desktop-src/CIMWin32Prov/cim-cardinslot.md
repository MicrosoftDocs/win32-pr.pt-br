---
description: A classe CIM \_ CardInSlot associa um cartão de adaptador ao contêiner no qual ele é inserido.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: CIM_CardInSlot classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2653160c536d9fd11668e5038ae632b09414cae42ed5ae76d998f3abda85eeec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322546"
---
# <a name="cim_cardinslot-class"></a>Classe CIM \_ CardInSlot

A **classe CIM \_ CardInSlot** associa um cartão de adaptador ao contêiner no qual ele é inserido.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ CardInSlot** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ CardInSlot** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Slot CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ Slot CIM**](cim-slot.md) que descreve o slot no qual o cartão é inserido.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cartão CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente"), [**Máx.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**cartão CIM \_**](cim-card.md) que descreve o cartão no slot.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ CardInSlot** é derivada de [**\_ PackageInSlot do CIM.**](cim-packageinslot.md)

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

[**Pacote \_ CIMInSlot**](cim-packageinslot.md)
</dt> </dl>

 

