---
description: A \_ associação CIM CardOnCard descreve as relações sobre os cartões que podem ser conectados a placas-mãe/placas, daughtercards de um adaptador ou cartões que dão suporte a módulos especiais semelhantes a cartões.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: Classe CIM_CardOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f6b20d95505f1e6dbbda31506660f3825541f8f2a0ecdcb6cf293d7d6d4a0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322436"
---
# <a name="cim_cardoncard-class"></a>\_Classe CIM CardOnCard

A associação **CIM \_ CardOnCard** descreve as relações sobre os cartões que podem ser conectados a placas-mãe/placas, daughtercards de um adaptador ou cartões que dão suporte a módulos especiais semelhantes a cartões.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ CardOnCard** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ CardOnCard** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ placa CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ cartão CIM**](cim-card.md) que descreve o cartão que hospeda outro cartão.

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

**MountOrSlotDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve e identifica como o cartão é montado ou conectado ao cartão "outro". As informações do slot podem ser incluídas nesse campo e podem ser suficientes para determinadas finalidades de gerenciamento, o que evita a criação de instanciações de objetos conector/slot apenas para modelar a relação de cartões para placas de hospedagem ou outros adaptadores. Por outro lado, se as informações de slot e conector estiverem disponíveis, esse campo poderá ser usado para fornecer dados detalhados de montagem ou de inserção de slot.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ placa CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Uma [**\_ placa CIM**](cim-card.md) que descreve o cartão que está conectado ou, de outra forma, montado em outro cartão.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ CardOnCard** é derivada do [**\_ contêiner CIM**](cim-container.md).

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

[**\_Contêiner CIM**](cim-container.md)
</dt> </dl>

 

