---
description: Uma classe abstrata para subclasses que descreve as capacidades de um elemento gerenciado associado e o potencial das habilidades.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: Classe CIM_Capabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787117"
---
# <a name="cim_capabilities-class"></a>\_Classe de recursos CIM

Uma classe abstrata para subclasses que descreve as capacidades de um elemento gerenciado associado e o potencial das habilidades.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Membros

A classe de **\_ recursos CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ recursos CIM** tem essas propriedades.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

O nome amigável do usuário para esta instância de classe. Além disso, o nome amigável do usuário pode ser usado como uma propriedade de índice para uma consulta. Esse valor não precisa ser exclusivo em seu namespace.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifica exclusivamente e de forma opaca uma instância dessa classe dentro do escopo do namespace que a contém.

> [!IMPORTANT]
>
> Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*
>
> *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida. Esse padrão é semelhante à estrutura de nomes de classe de esquema. Além disso, para garantir a exclusividade, os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*. Portanto, o *OrgID* não deve conter dois-pontos (': ').
>
> A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.
>
> Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.
>
> Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com o *OrgID* definido como CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Managedelement do CIM**](cim-managedelement.md)
</dt> </dl>

 

