---
description: A \_ classe de contêiner CIM representa uma associação entre um elemento físico contido e um que o contém. Um objeto recipiente deve ser um pacote físico.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: Classe CIM_Container
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0e4177fd70a79b1029d14ddb866eb533ce4c4e6183d88c61873bb9f8072a261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700756"
---
# <a name="cim_container-class"></a>\_Classe de contêiner CIM

A classe de **\_ contêiner CIM** representa uma associação entre um elemento físico contido e um que o contém. Um objeto recipiente deve ser um pacote físico.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a>Membros

A classe de **\_ contêiner CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ contêiner CIM** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que representa o pacote físico que contém outros elementos físicos, incluindo outros pacotes.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico. Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade. Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ físicoelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ físicoelement do CIM**](cim-physicalelement.md) que descreve o elemento físico que está contido no pacote.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas **do \_ contêiner CIM**, consulte [classes Win32](win32-provider.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

