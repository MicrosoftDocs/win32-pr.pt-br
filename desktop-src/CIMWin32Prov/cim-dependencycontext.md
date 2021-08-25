---
description: O \_ relacionamento CIM DependencyContext associa uma \_ classe de dependência CIM a um ou mais \_ objetos de configuração CIM. Por exemplo, as dependências de um sistema de computador podem ser alteradas com base na rede à qual o sistema está anexado.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Classe CIM_DependencyContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 845086b7d41eb03227d6b5b47240ef4bf9e1a2c35f8049c96d5c665800b327e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924636"
---
# <a name="cim_dependencycontext-class"></a>\_Classe CIM DependencyContext

O relacionamento **CIM \_ DependencyContext** associa uma classe de [**\_ dependência CIM**](cim-dependency.md) a um ou mais objetos de [**\_ configuração CIM**](cim-configuration.md) . Por exemplo, as dependências de um sistema de computador podem ser alteradas com base na rede à qual o sistema está anexado.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ DependencyContext** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ DependencyContext** tem essas propriedades.

<dl> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência ao objeto de configuração que agrega a dependência.

</dd> <dt>

**Dependência**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ dependência CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma dependência agregada.

</dd> </dl>

## <a name="remarks"></a>Comentários

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



 

