---
description: Representa o estado do componente de interface do serviço de convidado, que fornece um mecanismo para interagir com a máquina virtual a partir das interfaces de gerenciamento no sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Classe Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789803"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>\_Classe Msvm GuestServiceInterfaceComponent

Representa o estado do componente de interface do serviço de convidado, que fornece um mecanismo para interagir com a máquina virtual a partir das interfaces de gerenciamento no sistema host. Essa classe deriva da classe [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ GuestServiceInterfaceComponent** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Msvm \_ GuestServiceInterfaceComponent** tem esses métodos.



| Método                                                                               | Descrição                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Solicita que o estado do componente de interface do serviço de convidado seja alterado para o valor especificado.<br/>                           |
| [**Redefinir**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Solicita uma redefinição do dispositivo lógico. Não implementado pelo WMI.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado. Não implementado pelo WMI.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Msvm \_ GuestServiceInterfaceComponent** tem essas propriedades.

<dl> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Disponibilidade e status do dispositivo.



| Valor                                                                                                                                                                                                                                                                                                              | Significado                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Outros**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconhecido**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**Execução/energia completa**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Aviso**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**No teste**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Não aplicável**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Desligar**</dt> o <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Off line**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Fora do imposto**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Não instalado**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Erro de instalação**</dt> <dt>12 (0xc)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> Economia <dt>**de energia-**</dt> <dt>13 (0xD)</dt> desconhecido </dl>                             | O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> Economia <dt>**de energia-modo de baixa energia**</dt> <dt>14 (0xE)</dt> </dl> | O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> Economia <dt>**de energia-em espera**</dt> <dt>15 (0xF)</dt> </dl>                             | O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Ciclo de energia**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> Economia <dt>**de energia-aviso**</dt> <dt>17 (0x11)</dt> </dl>                            | O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.<br/>                              |



 

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Breve descrição textual do objeto. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Código de erro do Win32 Configuration Manager.



| Valor                                                                                | Significado                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | O dispositivo está funcionando corretamente.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | O dispositivo não está configurado corretamente.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | O Windows não pode carregar o driver para este dispositivo.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | O dispositivo não está funcionando corretamente. Um de seus drivers ou o registro pode estar corrompido.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Não é possível filtrar.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | O carregador de driver para o dispositivo está ausente.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | Não é possível iniciar o dispositivo.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Falha no dispositivo.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | O dispositivo não pode encontrar recursos livres suficientes para usar.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | O Windows não pode verificar os recursos do dispositivo.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | O dispositivo não funcionará corretamente até que o computador seja reiniciado.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | O Windows não pode identificar todos os recursos que o dispositivo usa.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | O dispositivo está solicitando um tipo de recurso desconhecido.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | Os drivers de dispositivo devem ser reinstalados.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Falha ao usar o carregador VxD.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | O registro pode estar corrompido.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Falha do sistema. Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware. O Windows está removendo o dispositivo.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | O dispositivo está desabilitado.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Falha do sistema. Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | O Windows ainda está configurando o dispositivo.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | O Windows ainda está configurando o dispositivo.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | O dispositivo não tem uma configuração de log válida.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | Os drivers de dispositivo não estão instalados.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Código do último erro relatado pelo dispositivo lógico.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.

Exemplo: " \* PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de recursos específicos relacionados à energia de um dispositivo lógico. Essa propriedade é herdada **de \_ LogicalDevice CIM**.



| Valor                                                                                                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconhecido**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Sem suporte**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Desabilitado**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Modos de economia de energia inseridos automaticamente**</dt> <dt>4 (0x4)</dt> </dl> | O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Estado de energia settable**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Há suporte para o método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) . Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado. Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Ciclo de energia com suporte**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | O método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Tempo de ativação com suporte de**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | O método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia. Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .

Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte. Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Status atual do objeto. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Os valores incluem o seguinte:

<dl><span id="OK"></span><span id="ok"></span><dt>

**PROBLEMAS**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Ao**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Degradado**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Conhecidos**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Falha de Pred"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Comece**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Impedir**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Serviço**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Analisa**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Não recuperar"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Sem contato"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Perda de comunicação"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado do dispositivo lógico. Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado. Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2 (0x2))
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3 (0x3))
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (4 (0x4))
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (5 (0x5))
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da classe de criação do sistema de escopo.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do sistema de escopo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> <dt>

[**\_LOGICALDEVICE CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

