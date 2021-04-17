---
description: A \_ classe CIM MemoryOnCard associa a memória física localizada em placas de hospedagem, placas de adaptador e assim por diante. Essa associação define explicitamente a relação de memória para os cartões.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: Classe CIM_MemoryOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755673"
---
# <a name="cim_memoryoncard-class"></a>\_Classe CIM MemoryOnCard

A classe **CIM \_ MemoryOnCard** associa a memória física localizada em placas de hospedagem, placas de adaptador e assim por diante. Essa associação define explicitamente a relação de memória para os cartões.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ MemoryOnCard** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ MemoryOnCard** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ placa CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ cartão CIM**](cim-card.md) que descreve o cartão que inclui ou ' contém ' memória.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico. Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade. Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .

Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalMemory**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ PhysicalMemory CIM**](cim-physicalmemory.md) que descreve a memória física que está localizada no cartão.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ MemoryOnCard** é derivada de [**\_ PackagedComponent CIM**](cim-packagedcomponent.md).

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

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> </dl>

 

