---
description: Usado para associar uma instância CIM RegisteredProfile a uma instância de CIM RegisteredProfile de outro perfil que faz referência ao perfil \_ dependente como um perfil \_ relacionado.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 39cfa6dac2fd827b2ce690afa5cdd7126322c2f81182db674517c75911791a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556805"
---
# <a name="cim_referencedprofile-class"></a>Classe CIM \_ ReferencedProfile

Usado para associar uma instância [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a uma instância de **CIM \_ RegisteredProfile** de outro perfil que faz referência ao perfil dependente como um perfil relacionado.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ReferencedProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ ReferencedProfile** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a [**instância \_ Cim RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) referenciada pelo **perfil** Dependente.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica uma instância [**\_ cim RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que faz referência a outros perfis.

</dd> </dl>

## <a name="remarks"></a>Comentários

O uso das propriedades **Dependent** e **Antecedent** na associação **CIM \_ ReferencedProfile** é definido de forma que o perfil que está sendo referenciado seja o antecessor e o perfil que faz a referência seja o dependente.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Interop \\ raiz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

