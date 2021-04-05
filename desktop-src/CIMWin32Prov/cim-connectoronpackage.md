---
description: A \_ classe CIM ConnectorOnPackage representa uma associação que torna explícita a relação de confinamento entre conectores e pacotes. Os pacotes físicos contêm conectores e outros elementos físicos.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: Classe CIM_ConnectorOnPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826496"
---
# <a name="cim_connectoronpackage-class"></a>\_Classe CIM ConnectorOnPackage

A classe **CIM \_ ConnectorOnPackage** representa uma associação que torna explícita a relação de confinamento entre conectores e pacotes. Os pacotes físicos contêm conectores e outros elementos físicos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ConnectorOnPackage** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ConnectorOnPackage** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico que tem um conector.

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

Tipo de dados: **CIM \_ PhysicalConnector**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que descreve o conector físico.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ ConnectorOnPackage** é derivada do [**\_ contêiner CIM**](cim-container.md).

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

 

