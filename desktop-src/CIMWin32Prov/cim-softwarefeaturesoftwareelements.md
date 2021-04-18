---
description: A \_ associação CIM SoftwareFeatureSoftwareElements identifica os elementos de software que compõem um recurso de software específico.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSoftwareElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756048"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a>\_Classe CIM SoftwareFeatureSoftwareElements

A associação **CIM \_ SoftwareFeatureSoftwareElements** identifica os elementos de software que compõem um recurso de software específico.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SoftwareFeatureSoftwareElements** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SoftwareFeatureSoftwareElements** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O componente de grupo.

Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ softwareelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O componente da parte.

Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A associação **CIM \_ SoftwareFeatureSoftwareElements** é derivada do [**\_ componente CIM**](cim-component.md).

O WMI não implementa essa classe. Para classes WMI derivadas do **CIM \_ SoftwareFeatureSoftwareElements**, consulte [classes Win32](win32-provider.md).

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

 

