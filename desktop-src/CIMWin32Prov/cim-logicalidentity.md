---
description: A \_ classe CIM LogicalIdentity é uma associação abstrata e genérica que indica que dois elementos lógicos representam diferentes aspectos da mesma entidade subjacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: Classe CIM_LogicalIdentity (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920228"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>Classe CIM_LogicalIdentity (provedores WMI CIMWin32)

A classe **CIM \_ LogicalIdentity** é uma associação abstrata e genérica que indica que dois elementos lógicos representam diferentes aspectos da mesma entidade subjacente. A associação transmite o que pode ser definido com várias heranças e é restrito aos aspectos lógicos de um elemento do sistema gerenciado. Na maioria dos cenários, a relação de identidade é determinada pela equivalência de chaves ou algumas outras propriedades de identificação dos elementos relacionados.

A associação só deve ser usada em cenários que são bem compreendidos, permitindo uma definição mais concreta e esclarecimento em subclasses. Um cenário em que a relação é razoável, por exemplo, representa um dispositivo que é uma entidade de barramento e uma entidade funcional em que o dispositivo é uma entidade USB (barramento) e teclado (funcional).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ LogicalIdentity** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ LogicalIdentity** tem essas propriedades.

<dl> <dt>

**Mesmoelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a um aspecto alternativo da entidade do sistema.

</dd> <dt>

**Sistema de**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a um aspecto do elemento lógico.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para classes derivadas do **CIM \_ LogicalIdentity**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




