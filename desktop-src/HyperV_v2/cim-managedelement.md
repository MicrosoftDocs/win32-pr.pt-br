---
description: A classe ManagedElement cim é uma classe abstrata que fornece uma superclasse comum (ou parte superior da árvore de herança) para as classes não associações no \_ esquema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: acce9925f057ab63e0697c2bc12cae4336533068afdf43f46322e4d3718b25c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648178"
---
# <a name="cim_managedelement-class"></a>Classe Cim \_ ManagedElement

A **classe \_ ManagedElement cim** é uma classe abstrata que fornece uma superclasse comum (ou parte superior da árvore de herança) para as classes não associações no esquema CIM.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a>Membros

A **classe \_ ManagedElement cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ManagedElement cim** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Uma breve descrição textual do objeto .

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição textual do objeto .

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome amigável para o objeto. Essa propriedade permite que cada instância de defina um nome amigável, além de suas propriedades de chave, dados de identidade e informações de descrição.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
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



 

