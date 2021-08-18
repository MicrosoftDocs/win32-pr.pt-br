---
description: Uma classe abstrata para subclasses que descreve as habilidades de um elemento gerenciado associado e o potencial das habilidades.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities classe
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
ms.openlocfilehash: 7fc640950b7e943f0e549f41ec216b2832ec9de3b91938ef1aadea1893ac2faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561906"
---
# <a name="cim_capabilities-class"></a>Classe De \_ funcionalidades CIM

Uma classe abstrata para subclasses que descreve as habilidades de um elemento gerenciado associado e o potencial das habilidades.

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

A **classe \_ Funcionalidades CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ Funcionalidades CIM** tem essas propriedades.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Obrigatório,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

O nome amigável para essa instância de classe. Além disso, o nome amigável do usuário pode ser usado como uma propriedade de índice para uma consulta. Esse valor não precisa ser exclusivo em seu namespace.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma exclusiva e opaca uma instância dessa classe dentro do escopo do namespace que o contém.

> [!IMPORTANT]
>
> Para garantir a exclusividade no namespace, o valor da **propriedade InstanceID** deve ser construído no seguinte padrão: *OrgID*:*LocalID*
>
> *OrgID* deve incluir um nome protegido por direitos autorais, marcas comerciais ou exclusivos pertencentes à entidade de negócios que define a **InstanceID** ou ser uma ID registrada atribuída por uma autoridade global reconhecida. Esse padrão é semelhante à estrutura de nomes de classe de esquema. Além disso, para garantir a exclusividade, os primeiros dois-pontos **em InstanceID** devem estar entre *o OrgID* e *o LocalID.* Portanto, *a OrgID* não deve conter dois-pontos (':').
>
> *LocalID* é escolhido pela entidade de negócios e não deve ser usado de novo para identificar diferentes elementos subjacentes do mundo real.
>
> Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor **de InstanceID** resultante não seja rea usado em nenhuma propriedade **InstanceID** produzida por esse provedor ou outros provedores para esse namespace.
>
> Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com *o OrgID* definido como CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ManagedElement do CIM \_**](cim-managedelement.md)
</dt> </dl>

 

