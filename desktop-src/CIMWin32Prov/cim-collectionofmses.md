---
description: O objeto Cim CollectionOfMSEs permite o agrupamento de objetos Cim ManagedSystemElement com a finalidade de associar configurações \_ \_ e configurações. É abstrato exigir definição e refinamento semânticos em subclasses.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs classe (Provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d67b51e90a9a3c2eff420a5251c1b4e75f323d48e796a3190b662fb844c1517a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579046"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs classe (Provedores WMI CIMWin32)

O **objeto \_ Cim CollectionOfMSEs** permite o agrupamento de objetos [**Cim \_ ManagedSystemElement**](cim-managedsystemelement.md) com a finalidade de associar configurações e configurações. É abstrato exigir definição e refinamento semânticos em subclasses.

O **objeto \_ Cim CollectionOfMSEs** não carrega nenhuma informação de estado ou status, mas representa apenas um grupo de elementos. Por esse motivo, está incorreto para grupos de subclasses que têm estado/status de **Cim \_ CollectionOfMSEs**, um exemplo é [**Cim \_ RedundancyGroup**](cim-redundancygroup.md) (que é corretamente subclasse de [**CIM \_ LogicalElement**](cim-logicalelement.md)). As coleções normalmente agregam objetos 'like' e representam uma otimização. Sem coleções, uma é forçada a definir associações [**individuais \_ de ElementSetting**](cim-elementsetting.md) e [**\_ ElementConfiguration cim cim,**](cim-elementconfiguration.md) para ligar configurações e objetos de configuração a [**\_ managedsystemelements cim individuais.**](cim-managedsystemelement.md) Pode haver muita duplicação na atribuição da mesma configuração a vários objetos. Além disso, o uso do objeto de coleção permite a determinação de que as associações de configuração e configuração são realmente as mesmas para os membros da coleção. Caso contrário, essas informações seriam obtidas definindo a coleção de maneira proprietária e consultando as associações **\_ ElementSetting e** **Cim \_ ElementConfiguration** para determinar se o conjunto de coleta é completamente coberto.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ CollectionOfMSEs** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CIM CollectionOfMSEs** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual curta do objeto CollectionOfMSEs.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificação do objeto Coleção. Quando subclasse, a propriedade CollectionID pode ser substituído para ser uma propriedade Key.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto CollectionOfMSEs.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Consulte [Classes Win32 para](win32-provider.md) classes WMI derivadas de Coleção **\_ CIMOfMSEs**.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




