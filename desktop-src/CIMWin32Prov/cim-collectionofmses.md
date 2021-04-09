---
description: O \_ objeto CIM CollectionOfMSEs permite o agrupamento de \_ objetos CIM ManagedSystemElement com a finalidade de associar definições e configurações. É abstrato exigir mais definição e refinamento semântico em subclasses.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfMSEs (provedores WMI CIMWin32)
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
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089351"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>Classe CIM_CollectionOfMSEs (provedores WMI CIMWin32)

O objeto **CIM \_ CollectionOfMSEs** permite o agrupamento de objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) com a finalidade de associar definições e configurações. É abstrato exigir mais definição e refinamento semântico em subclasses.

O objeto **CIM \_ CollectionOfMSEs** não carrega nenhuma informação de estado ou status, mas representa apenas um agrupamento de elementos. Por esse motivo, ele está incorreto para grupos de subclasses que têm estado/status do **CIM \_ CollectionOfMSEs**, um exemplo é o [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (que é subclasse corretamente de [**CIM \_ LogicalElement**](cim-logicalelement.md)). Normalmente, as coleções agregam objetos ' like ' e representam uma otimização. Sem coleções, uma é forçada a definir as associações [**\_ ElementSetting**](cim-elementsetting.md) e CIM [**\_ ElementConfiguration**](cim-elementconfiguration.md) individuais para vincular configurações e objetos de configuração a [**\_ ManagedSystemElements CIM**](cim-managedsystemelement.md)individuais. Pode haver muita duplicação ao atribuir a mesma configuração a vários objetos. Além disso, o uso do objeto de coleção permite determinar se as associações de configuração e configuração são realmente as mesmas para os membros da coleção. Por outro lado, essas informações seriam obtidas definindo a coleção de forma proprietária e, em seguida, consultando as associações **CIM \_ ElementSetting** e **CIM \_ ElementConfiguration** para determinar se o conjunto de coleta foi totalmente coberto.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

A classe **CIM \_ CollectionOfMSEs** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ CollectionOfMSEs** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Breve descrição textual do objeto CollectionOfMSEs.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificação do objeto de coleção. Quando em uma subclasse, a propriedade CollectionId pode ser substituída para ser uma propriedade de chave.

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

O WMI não implementa essa classe. Consulte [classes Win32](win32-provider.md) para classes WMI derivadas do **CIM \_ CollectionOfMSEs**.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




