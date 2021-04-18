---
description: Representa uma associação entre um elemento gerenciado e seus dados de configuração associados. Essa associação também descreve se esta é uma configuração padrão ou atual.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Classe CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780541"
---
# <a name="cim_elementsettingdata-class"></a>\_Classe CIM ElementSettingData

Representa uma associação entre um elemento gerenciado e seus dados de configuração associados. Essa associação também descreve se esta é uma configuração padrão ou atual.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ElementSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ElementSettingData** tem essas propriedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada está sendo usada no momento pelo elemento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**Está atual** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**Não é atual** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indicando se a configuração é uma configuração padrão para o elemento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

**É padrão** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**Não é o padrão** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Isnext**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um sinalizador que indica quando e com que frequência aplicar a configuração.

Por exemplo, a configuração pode ser aplicada em uma solicitação de reinicialização, redefinição e reconfiguração. Essa pode ser uma configuração permanente ou uma configuração usada apenas uma vez, conforme indicado pelo sinalizador. Se for uma configuração permanente, a configuração será aplicada toda vez que o elemento gerenciado for reinicializado, até que esse sinalizador seja redefinido manualmente. No entanto, se for um uso único, o sinalizador será limpo automaticamente depois que as configurações forem aplicadas. Além disso, se esse sinalizador for definido com um valor diferente de 0 (desconhecido), isso terá precedência sobre uma propriedade **SettingData** definida como "padrão".

Se o elemento gerenciado for um sistema de computador, e o valor desse sinalizador for "Next", a configuração entrará em vigor na próxima vez que o sistema for redefinido. E, a menos que esse sinalizador seja alterado, ele será mantido para redefinições subsequentes do sistema. No entanto, se esse sinalizador for definido como "é próximo para uso único", essa configuração será usada apenas uma vez e o sinalizador será redefinido depois disso para 2 (não é próximo). Portanto, no exemplo acima, se o sistema reinicializar em uma rápida sucessão, a configuração não será usada na segunda reinicialização.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**É próximo** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**Não é próximo** (2)


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**É o próximo para uso único** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O elemento gerenciado.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Os dados de configuração associados ao elemento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

