---
description: A classe CIM \_ BIOSFeatureBIOSElements associa um recurso BIOS e seus elementos BIOS agregados.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: CIM_BIOSFeatureBIOSElements classe
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
ms.openlocfilehash: 7af2928625084b84ceff8895f15b5b426ebe82105074401c4bbab7eba46f3e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701016"
---
# <a name="cim_biosfeaturebioselements-class"></a>Classe CIM \_ BIOSFeatureBIOSElements

A **classe CIM \_ BIOSFeatureBIOSElements** associa um recurso BIOS e seus elementos BIOS agregados.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

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

A **classe CIM \_ BIOSFeatureBIOSElements** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ BIOSFeatureBIOSElements** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ BIOSFeature**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Um [**CIM \_ BIOSFeature**](cim-biosfeature.md) que descreve o recurso BIOS.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ BIOSElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**CIM \_ BIOSElement**](cim-bioselement.md) que descreve o elemento BIOS que implementa os recursos descritos pelo recurso BIOS.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ BIOSFeatureBIOSElements** é derivada de [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).

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

[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

