---
description: Representa o software de nível baixo que é carregado na RAM para configurar e iniciar o sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Classe Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827387"
---
# <a name="msvm_bioselement-class"></a>\_Classe bioselement Msvm

Representa o software de nível baixo que é carregado na RAM para configurar e iniciar o sistema. O BIOS não é um dispositivo lógico, portanto, o BIOS virtual não deve ser considerado um dispositivo de máquina virtual. Como não é um dispositivo, ele não tem um pool de recursos correspondente. O objeto BIOS é associado à máquina virtual por meio da Associação [**Msvm \_ SystemBIOS**](msvm-systembios.md) .

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>Membros

A **classe \_ bioselement Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ bioselement Msvm** tem essas propriedades.

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de série da placa base na máquina virtual.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O identificador exclusivo para o BIOS.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado habilitado do bloqueio num no BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de série do BIOS.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

A ordem em que os dispositivos serão pesquisados em um setor de inicialização na inicialização.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

O identificador interno para esta compilação do elemento de software. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como 14.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Preenchido automaticamente pelo BIOS quando a máquina virtual é criada.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Preenchido automaticamente pelo BIOS quando a máquina virtual é criada.

</dd> <dt>

**Código de**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

O conjunto de códigos usado pelo elemento software. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O idioma selecionado no momento para o BIOS. Essa propriedade é herdada de [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "en \| US \| ISO8859-1".

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o elemento. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a integridade atual do elemento. Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.

Quando ocorrer um erro crítico, verifique o log de eventos para obter detalhes. A propriedade **enabledstate** também pode conter mais informações. Por exemplo, quando o espaço em disco está muito baixo, o **HealthState** é definido como 25, a máquina virtual pausa e **enabledstate** é definido como 32768 (em pausa).

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Valor                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | A máquina virtual é totalmente funcional e está operando em parâmetros operacionais normais e sem erros.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Maior falha**</dt> <dt>20</dt> </dl>             | A máquina virtual sofreu uma falha grave. Esse valor é usado quando um ou mais discos que contêm VHDs da máquina virtual estão com pouco espaço em disco e a máquina virtual foi pausada.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Falha crítica**</dt> <dt>25</dt> </dl> | O elemento não é funcional e a recuperação pode não ser possível. Isso pode indicar que o processo de trabalho para a máquina virtual (Vmwp.exe) não está respondendo às solicitações de controle ou de informações, ou que um ou mais discos que contêm VHDs para a máquina virtual estão com pouco espaço em disco.<br/> |



 

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

O identificador do fabricante para este elemento de software. Geralmente, essa será uma SKU (unidade de manutenção de estoque) ou um número de peça. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Preenchido automaticamente pelo BIOS quando a máquina virtual é criada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (32)
</dt> </dl>

A edição de idioma deste elemento de software. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de idiomas instaláveis para o BIOS. Essa propriedade é herdada de [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "en \| US \| ISO8859-1".

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **unit64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço final da memória que este BIOS ocupa. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como 0xFFFFF.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **unit64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço inicial da memória que este BIOS ocupa. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como 0xE0000.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o Utilitário Flash/Load do BIOS que é necessário para atualizar o elemento BIOS. A versão e outras informações podem ser indicadas nesta propriedade. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como **NULL**.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (256)
</dt> </dl>

O fabricante deste BIOS. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "Microsoft Corporation".

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (1024)
</dt> </dl>

O nome usado para identificar este elemento de software. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como "BIOS".

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** . Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém os status atuais do objeto. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). O valor no índice zero (0) é um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | A máquina virtual está funcional e funcionando normalmente.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>3</dt> </dl>                                         | A máquina virtual só está parcialmente funcional. Isso indica que o armazenamento que contém a configuração não está acessível. Uma máquina virtual nesse estado só pode ser desativada ou excluída. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Falha preditiva**</dt> <dt>5</dt> </dl> | A máquina virtual é funcional, mas pode falhar no futuro. Isso indica que o armazenamento que contém o disco rígido virtual da máquina virtual está com pouco espaço livre. A máquina virtual será pausada se mais espaço em disco não for disponibilizado.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Parado**</dt> <dt>10</dt> </dl>                                            | Não há suporte para esse valor. Se a máquina virtual for interrompida, a propriedade **enabledstate** terá um valor de 3 (desabilitado).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**No serviço**</dt> <dt>11</dt> </dl>                                | A máquina virtual está processando uma solicitação.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>15</dt> <dt>**inativos**</dt> </dl>                                            | Não há suporte para esse valor. Se a máquina virtual for suspensa ou pausada, a propriedade **enabledstate** terá um valor de 32769 (suspenso) ou 32768 (em pausa).<br/>                                                                                    |



 

O valor no índice one (1) é opcional e contém informações de status secundárias. Um cliente deve usar o status principal do índice zero (0) para determinar se uma nova solicitação pode ser emitida para a máquina virtual. Se **OperationalStatus** \[ 0 \] for 2 (OK), a operação indicada por **OperationalStatus** \[ 1 \] poderá ser interrompida.

O valor em **OperationalStatus** \[ 1 \] é um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Criando o instantâneo**</dt> <dt>32768</dt> </dl>                                 | Um instantâneo está em processo de criação para a máquina virtual.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Aplicando o instantâneo**</dt> <dt>32769</dt> </dl>                                 | Um instantâneo está no processo de ser aplicado à máquina virtual.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Excluindo o instantâneo**</dt> <dt>32770</dt> </dl>                                 | Um instantâneo está no processo de ser excluído da máquina virtual.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Aguardando para iniciar**</dt> o <dt>32771</dt> </dl>                                     | A máquina virtual será iniciada depois que o atraso de inicialização automática tiver decorrido.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Mesclando discos**</dt> <dt>32772</dt> </dl>                                                 | Os discos rígidos virtuais dos instantâneos excluídos anteriormente estão sendo mesclados.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportando a máquina Virtual**</dt> <dt>32773</dt> </dl> | A máquina virtual está sendo exportada.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrando a máquina Virtual**</dt> <dt>32774</dt> </dl> | A máquina virtual está sendo migrada ao vivo de um computador físico para outro.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

O fabricante e o sistema operacional de um elemento de software quando a propriedade **TargetOperatingSystem** tem um valor de 1 (outro), que exige que a propriedade **OtherTargetOS** tenha um valor não **nulo** . Para todos os outros valores de **TargetOperatingSystem**, a propriedade **OtherTargetOS** deve ser **NULL**. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for true, esse é o BIOS primário do sistema de computador. Essa propriedade é herdada de [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como **true**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status de alto nível. Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres que representa o local de publicação do registro de atributo do BIOS ou registros em conformidade com a implementação. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**Liberado**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data em que o BIOS foi lançado. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

O número de série atribuído do BIOS. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (256)
</dt> </dl>

Um identificador para o elemento de software. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como "Microsoft:*GUID* \\ *específico de dispositivo-dados*".

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado do ciclo de vida de um elemento de software. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como 2 (executável).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ArrayType** ("indexado")
</dt> </dl>

Uma matriz que contém cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** . Por exemplo, se 11 (em serviço) for o valor atribuído a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] poderá conter uma explicação sobre o motivo pelo qual a máquina virtual está processando uma solicitação. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O ambiente do sistema operacional do elemento. Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como 0 (desconhecido).

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

A versão do BIOS. Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "8.02.00".

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ bioselement Msvm** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ bioselement**](cim-bioselement.md)
</dt> <dt>

[Classes do BIOS](bios-classes.md)
</dt> <dt>

[**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

