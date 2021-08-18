---
description: Representa um serviço de dispositivo virtual da plataforma Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent classe
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
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340166"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>Classe Msvm \_ VirtualSystemResourceComponent

Representa um serviço de dispositivo virtual da plataforma Microsoft Windows Hyper-V.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe \_ VirtualSystemResourceComponent Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ VirtualSystemResourceComponent Msvm** tem essas propriedades.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres que contém classes adicionais que não são de associação superfície por essa instância **\_ virtualSystemResourceComponent da Msvm.** Essas classes não devem derivar de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nem [**cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um GUID que representa o identificador de classe do objeto COM do serviço. Essa propriedade é herdada [**de Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O contexto no qual o objeto recém-criado será executado. Esse valor é passado no parâmetro *dwClsContext* para [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Essa propriedade é herdada [**de Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como 1.

</dd> <dt>

**Habilitada**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se essa instância estiver habilitada e puder ser usada para concluir solicitações de cliente; caso contrário, **False.** Essa propriedade é herdada [**de Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como **True.**

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se essa instância puder ser adicionada a uma máquina virtual; caso contrário, **False.** O padrão é **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se essa instância puder ser removida a quente de uma máquina virtual; caso contrário, **False.** O padrão é **False**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Uma cadeia de caracteres neutra em idioma que identifica exclusivamente o serviço. O formato a seguir é sugerido para evitar conflitos de nomen por nome: "versão \| do componente \| do fornecedor". Por exemplo, esse nome representa a versão 1.0 do Componente de Porta de Rede Emulada da Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Essa propriedade é herdada [**de Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A relação do objeto WMI descrito aqui com o dispositivo virtual.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Não Changeable"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton é um objeto WMI de nível superior que está vinculado 1:1 a um Dispositivo Virtual e só pode existir uma vez por máquina virtual. Esse é o valor padrão.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"MultiInstance"**</dt> <dt>2</dt> </dl>     | MultiInstance é um objeto WMI de nível superior que pode existir várias vezes por máquina virtual e está vinculado a 1:1 com um Dispositivo Virtual.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdevice"**</dt> <dt>3</dt> </dl>                     | O subdevice é um objeto WMI que não tem referência pai, mas é controlado por apenas um Dispositivo Virtual que pode existir apenas uma vez por máquina virtual. No entanto, o objeto WMI pode existir várias vezes.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ VirtualSystemResourceComponent do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Fim do suporte ao cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fim do suporte ao servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

