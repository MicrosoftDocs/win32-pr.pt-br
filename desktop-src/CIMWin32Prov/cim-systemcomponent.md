---
description: Uma classe de associação de modelo CIM (CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: Classe CIM_SystemComponent (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089347"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a>Classe CIM_SystemComponent (provedores WMI CIMWin32)

A classe **CIM \_ Systemcomponent** é uma classe de associação de modelo CIM (CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ Systemcomponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ Systemcomponent** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema pai na associação.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento filho que é um componente de um sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para classes WMI derivadas do **CIM \_ Systemcomponent**, consulte [classes Win32](win32-provider.md).

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

 

