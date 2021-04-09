---
description: A \_ classe CIM BIOSFeatureBIOSElements associa um recurso do BIOS e seus elementos do BIOS agregados.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeatureBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089395"
---
# <a name="cim_biosfeaturebioselements-class"></a>\_Classe CIM BIOSFeatureBIOSElements

A classe **CIM \_ BIOSFeatureBIOSElements** associa um recurso do BIOS e seus elementos do BIOS agregados.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ BIOSFeatureBIOSElements** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ BIOSFeatureBIOSElements** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ BIOSFeature**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Um [**\_ BIOSFeature CIM**](cim-biosfeature.md) que descreve o recurso do BIOS.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ bioselement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**CIM \_ bioselement**](cim-bioselement.md) que descreve o elemento BIOS que implementa os recursos descritos pelo recurso do BIOS.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ BIOSFeatureBIOSElements** é derivada de [**\_ SoftwareFeatureSoftwareElements CIM**](cim-softwarefeaturesoftwareelements.md).

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

[**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

