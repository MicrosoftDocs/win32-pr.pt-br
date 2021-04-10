---
description: Representa parâmetros operacionais e de configuração para \_ instâncias de CIM managedelement.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Classe CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170068"
---
# <a name="cim_settingdata-class"></a>Classe do CIM \_ SettingData

Representa parâmetros operacionais e de configuração para instâncias de [**CIM \_ managedelement**](cim-managedelement.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Membros

A classe do **CIM \_ SettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SettingData** tem essas propriedades.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

O nome amigável para uma instância desta classe. Além disso, o nome amigável do usuário pode ser usado como um índice para uma pesquisa ou consulta. O nome não precisa ser exclusivo em um namespace.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifica exclusivamente uma instância dessa classe dentro do escopo do namespace que a contém.

> [!IMPORTANT]
>
> Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*
>
> -   *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a propriedade **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.
> -   *OrgID* não deve conter dois-pontos. Os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.
> -   A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.
> -   Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.
> -   Para instâncias definidas por DMTF, o padrão deve ser usado com o *OrgID* definido como "CIM".

 

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

 

