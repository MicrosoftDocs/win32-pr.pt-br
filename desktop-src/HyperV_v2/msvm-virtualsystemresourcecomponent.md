---
description: Representa um serviço de dispositivo virtual da plataforma Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Classe Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780973"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>\_Classe Msvm VirtualSystemResourceComponent

Representa um serviço de dispositivo virtual da plataforma Microsoft Windows Hyper-V.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemResourceComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemResourceComponent** tem essas propriedades.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres que contém classes de não associação adicionais superfícieda por essa instância de **\_ VirtualSystemResourceComponent de Msvm** . Essas classes devem derivar de [**nenhum \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nem de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um GUID que representa o identificador de classe do objeto COM do serviço. Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O contexto no qual o objeto recém-criado será executado. Esse valor é passado no parâmetro *dwClsContext* para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se esta instância estiver habilitada e puder ser usada para concluir solicitações de cliente; caso contrário, **false**. Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como **true**.

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se esta instância puder ser adicionada em uma máquina virtual; caso contrário, **false**. O padrão é **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se esta instância puder ser removida de uma máquina virtual; caso contrário, **false**. O padrão é **False**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Uma cadeia de caracteres neutra em idioma que identifica exclusivamente o serviço. O seguinte formato é sugerido para evitar conflitos de nomenclatura: " \| versão do componente do fornecedor \| ". Por exemplo, esse nome representa a versão 1,0 do componente de porta de rede emulada da Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0". Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A relação do objeto WMI que é descrita aqui com o dispositivo virtual.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Não alterado"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton é um objeto WMI de nível superior que está vinculado 1:1 a um dispositivo virtual e só pode existir uma vez por máquina virtual. Esse é o valor padrão.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"MultiInstance"**</dt> <dt>2</dt> </dl>     | MultiInstance é um objeto WMI de nível superior que pode existir várias vezes por máquina virtual e está vinculado 1:1 a um dispositivo virtual.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdispositivo"**</dt> <dt>3</dt> </dl>                     | O subdispositivo é um objeto WMI que não tem referência pai, mas é controlado por apenas um dispositivo virtual que pode existir apenas uma vez por máquina virtual. Embora o objeto WMI possa existir várias vezes.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualSystemResourceComponent** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Fim do suporte do cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

