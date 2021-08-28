---
description: Usado no método GetSummaryInformation na \_ classe VirtualSystemManagementService Msvm para recuperar rapidamente informações comuns relacionadas a um instantâneo ou um sistema virtual.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Classe Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd99ec5a0a9f3bd4bd07fa88cfc15139c69a442b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886572"
---
# <a name="msvm_summaryinformationbase-class"></a>\_Classe Msvm SummaryInformationBase

Usado no método [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) na classe [**\_ VirtualSystemManagementService Msvm**](msvm-virtualsystemmanagementservice.md) para recuperar rapidamente informações comuns relacionadas a um instantâneo ou um sistema virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SummaryInformationBase** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SummaryInformationBase** tem essas propriedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que o sistema virtual ou o instantâneo foi criado.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managedelement. ElementName")
</dt> </dl>

O nome amigável para o instantâneo ou o sistema virtual.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado atual do instantâneo ou do sistema virtual.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se as conexões de modo avançado são permitidas ou não pelo host e se são permitidas, se elas estão disponíveis para a máquina virtual.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Permitido e disponível** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Não permitido** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Permitido, mas não disponível** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado de integridade atual do sistema virtual. Esta propriedade não é válida para instâncias de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) representando um instantâneo do sistema virtual.

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do computador que hospeda esta máquina virtual.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managedelement. InstanceId"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID é uma propriedade opcional que pode ser usada para identificar de forma opaca e exclusiva uma instância dessa classe dentro do escopo do namespace de instanciação. Várias subclasses dessa classe podem substituir essa propriedade para torná-la necessária ou uma chave. Essas subclasses também podem modificar os algoritmos preferenciais para garantir a exclusividade definida abaixo.

Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial":

&lt;OrgID &gt; : &lt; LocalId&gt;

Onde &lt; OrgID &gt; e &lt; LocalId &gt; são separados por dois-pontos (:), e onde &lt; OrgID &gt; deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida. (Esse requisito é semelhante ao <Schema Name> \_ <Class Name> estrutura de nomes de classe de esquema.) Além disso, para garantir a exclusividade, &lt; OrgID &gt; não deve conter dois-pontos (:). Ao usar esse algoritmo, os primeiros dois-pontos para aparecer em InstanceID devem aparecer entre &lt; OrgID &gt; e &lt; LocalId &gt; .

&lt;A localId &gt; é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos subjacentes (reais) diferentes. Se não for nulo e o algoritmo "preferencial" acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por este ou outros provedores para o NameSpace dessa instância.

Se não estiver definido como nulo para instâncias definidas por DMTF, o algoritmo "preferencial" deverá ser usado com o &lt; OrgID &gt; definido como CIM.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome exclusivo para o sistema virtual ou instantâneo.

</dd> <dt>

**Observações**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As notas associadas ao sistema virtual ou instantâneo.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número total de processadores virtuais alocados para o sistema virtual ou instantâneo.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

O status atual do elemento.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other"). Essa propriedade deve ser definida como NULL quando **enabledstate** for qualquer valor diferente de 1.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .

</dd> <dt>

**Atividade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade de tempo desde a última inicialização do sistema virtual. Esta propriedade não é válida para instâncias de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) representando um instantâneo do sistema virtual.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão do sistema virtual em um formato de "Major. Minor"; por exemplo, "2,0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Cadeias de caracteres que listam os nomes amigáveis dos comutadores virtuais aos quais a VM está conectada.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O subtipo do sistema virtual.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Exibição CIM \_**](cim-view.md)
</dt> </dl>

 

