---
description: Uma \_ classe de sistema CIM representa uma coleção especial de \_ instâncias do CIM ManagedSystemElement.
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystem (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457078"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a>Classe CIM_ComputerSystem (provedores WMI CIMWin32)

Uma classe de **\_ sistema CIM** representa uma coleção especial de instâncias do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) . Esta coleção fornece recursos do computador e serve como um ponto de agregação para associar um ou mais dos seguintes elementos: sistema de arquivos, sistema operacional, processador e memória (armazenamento volátil e não volátil). Essa classe é derivada do [**\_ sistema CIM**](cim-system.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a>Membros

A classe de **\_ sistema CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ ComputerSystem de CIM** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Define o rótulo pelo qual o objeto é conhecido.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Identifica como o nome do sistema de computador é gerado, usando uma heurística. A heurística é descrita em detalhes na especificação de modelo comum do CIM v2. Ele pressupõe que as regras documentadas são percorridas em ordem, para determinar e atribuir um nome. A lista de valores **NameFormat** define a ordem de precedência para atribuir o nome do sistema do computador. Várias regras são mapeadas para o mesmo valor.

Observe que o **nome** do objeto é calculado usando o heurístico é o valor de chave do sistema. Outros nomes podem ser atribuídos e usados para o objeto que melhor atendam aos negócios, usando aliases.

<dt>

<span id="IP"></span><span id="ip"></span>

**IP** ("IP")


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Discar** ("discar")


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** ("HID")


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**NWA** ("NWA")


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**Hwa** ("Hwa")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("X25")


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** ("ISDN")


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** ("IPX")


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**DCC** ("DCC")


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E. 164** ("E. 164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** ("outro")


</dt> <dd></dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone ou endereço de email).

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome do proprietário do sistema primário.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**Funções**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

As funções que o sistema desempenha no ambiente de tecnologia da informação. As subclasses do sistema podem substituir essa propriedade para definir valores de função explícitos. Como alternativa, um grupo de trabalho pode descrever a heurística, as convenções e as diretrizes para especificar funções. Por exemplo, para uma instância de um sistema de rede, essa propriedade pode conter a cadeia de caracteres "switch" ou "Bridge".

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ ComputerSystem do CIM** é derivada do [**\_ sistema CIM**](cim-system.md).

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas do **CIM \_ ComputerSystem**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Sistema CIM**](cim-system.md)
</dt> </dl>

 

