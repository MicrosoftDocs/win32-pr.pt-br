---
description: A \_ relação de SlotInSlot do CIM representa a capacidade de um adaptador especial estender a estrutura de slot existente para permitir que cartões incompatíveis sejam conectados a um quadro ou placa de hospedagem.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Classe CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749322"
---
# <a name="cim_slotinslot-class"></a>\_Classe CIM SlotInSlot

A relação de **\_ SlotInSlot do CIM** representa a capacidade de um adaptador especial estender a estrutura de slot existente para permitir que cartões incompatíveis sejam conectados a um quadro ou placa de hospedagem. Os slots são tipos especiais de conectores nos quais as placas de adaptador são normalmente inseridas. O adaptador cria efetivamente um novo slot e pode ser considerado (conceitualmente) como um slot em um slot. Os cartões que, de outra forma, seriam incompatíveis fisicamente ou eletricamente com os slots existentes seriam compatíveis com a interface do slot fornecido pelo adaptador. Por exemplo, as placas de rede são muito caras. À medida que um novo hardware é disponibilizado, as configurações do chassi e do cartão são alteradas. Para proteger o investimento de seus clientes, os fornecedores de rede fabricarão adaptadores especiais que permitem que os cartões antigos se encaixem em novos chassis ou placas de hospedagem ou novos cartões para se ajustarem em cartões antigos usando um adaptador especial que caiba em um ou mais slots existentes e apresente um novo slot ao qual o cartão pode se ajustar.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SlotInSlot** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SlotInSlot** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ slot CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ slot CIM**](cim-slot.md) que descreve os slots existentes da placa de hospedagem ou o quadro que está sendo adaptado para acomodar um cartão que, de outra forma, não seria fisicamente e/ou eletricamente compatível com ele.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ slot CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Um [**\_ slot CIM**](cim-slot.md) que descreve o novo slot fornecido pela placa adaptadora.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ SlotInSlot** é derivada de [**CIM \_ conectado**](cim-connectedto.md)a.

O WMI não implementa essa classe.

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

[**CIM \_ conectado**](cim-connectedto.md)
</dt> </dl>

 

