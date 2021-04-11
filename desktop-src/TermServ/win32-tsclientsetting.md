---
title: Classe Win32_TSClientSetting
description: Define as definições de configuração para a \_ classe de terminal Win32 relacionada à política de conexão.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSClientSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSClientSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086274"
---
# <a name="win32_tsclientsetting-class"></a>\_Classe Win32 TSClientSetting

A classe WMI **\_ TSClientSetting do Win32** define as definições de configuração para a classe de [**\_ terminal Win32**](win32-terminal.md) relacionada à política de conexão.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSClientSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSClientSetting** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Define as propriedades **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** e **DefaultToClientPrinter** dessa classe.<br/>                      |
| [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md)                 | Não há suporte.<br/> **Windows 7 e Windows Server 2008 R2:** Define a propriedade **AllowDwm** .<br/>                                               |
| [**Setclientproperty**](win32-tsclientsetting-setclientproperty.md)     | Define a propriedade **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** .<br/> |
| [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md)             | Define a propriedade **ColorDepth** .<br/>                                                                                                                 |
| [**SetColorDepthPolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | Define a propriedade **ColorDepthPolicy** .<br/>                                                                                                           |
| [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md)           | Define a propriedade **MaxMonitors** .<br/>                                                                                                                |
| [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md)     | Define a propriedade **MaxXResolution** .<br/>                                                                                                             |
| [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md)     | Define a propriedade **MaxYResolution** .<br/>                                                                                                             |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSClientSetting** tem essas propriedades.

<dl> <dt>

**AdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se é para habilitar gráficos RemoteFX avançados para o RemoteApp.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2012 R2 e Windows 8.1.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Os gráficos avançados estão desabilitados.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

Os gráficos avançados estão habilitados.

</dd> </dl>

</dd> <dt>

**AllowDwm**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Esta propriedade não está disponível.

* * Windows 7 e Windows Server 2008 R2: * *

Especifica se a composição da área de trabalho remota deve ser habilitada ou desabilitada. Zero desabilitará a composição de área de trabalho remota e um valor diferente de zero permitirá isso.

Use o método [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) para modificar essa propriedade.

</dd> <dt>

**AudioCaptureRedir**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o redirecionamento de captura de áudio deve ser permitido.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**Verdadeiro** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**AudioMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o mapeamento de áudio está desabilitado ou habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O mapeamento de áudio está habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O mapeamento de áudio está desabilitado.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o modo AVC444 é preferencial.

**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows Server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 10 ou do Windows Server 2016.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**Verdadeiro** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição (cadeia de caracteres de uma linha) do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ClipboardMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o mapeamento da área de transferência está desabilitado ou habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O mapeamento da área de transferência está habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O mapeamento da área de transferência está desabilitado.

</dd> </dl>

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a profundidade de cor. Para obter os valores possíveis, consulte o método [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 bits** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 bits** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 bits** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 bits** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**32 bits** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se a configuração de cor máxima do usuário deve ser substituída.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Não substitua a política do usuário.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

Substituir a política do usuário.

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o mapeamento de porta COM está desabilitado ou habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O mapeamento de porta COM está habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O mapeamento de porta COM está desabilitado.

</dd> </dl>

</dd> <dt>

**ConnectClientDrivesAtLogon**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se as unidades do cliente serão conectadas automaticamente durante o processo de logon.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

As unidades não serão conectadas automaticamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

As unidades serão conectadas automaticamente.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A política que o servidor usa para recuperar as configurações de conexão do usuário.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)


</dt> <dd>

As configurações de conexão do usuário estão em vigor.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)


</dt> <dd>

As configurações de conexão do usuário são substituídas pelo servidor.

</dd> </dl>

</dd> <dt>

**ConnectPrinterAtLogon**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se todas as impressoras locais mapeadas do cliente serão conectadas automaticamente durante o processo de logon.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

As impressoras locais não serão conectadas automaticamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

As impressoras locais serão conectadas automaticamente.

</dd> </dl>

</dd> <dt>

**DefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se os trabalhos de impressão serão enviados automaticamente para a impressora local do cliente.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Os trabalhos de impressão não devem ser enviados automaticamente para a impressora local do cliente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

Os trabalhos de impressão devem ser enviados automaticamente para a impressora local do cliente.

</dd> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DriveMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o mapeamento de unidade está desabilitado ou habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O mapeamento de unidade está habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O mapeamento de unidade está desabilitado.

</dd> </dl>

</dd> <dt>

**EncodeImageQuality**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica a qualidade da imagem para a experiência RDP.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

**sem perdas** (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**alta** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**médio** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o servidor de Host da Sessão RD usa o processador de gráficos de hardware como o adaptador padrão.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**Verdadeiro** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")
</dt> </dl>

A data em que o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LPTPortMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o mapeamento de porta LPT está desabilitado ou habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O mapeamento de porta LPT está habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O mapeamento de porta LPT está desabilitado.

</dd> </dl>

</dd> <dt>

**MaxMonitors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número máximo de monitores com suporte no servidor. Use o método [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) para modificar essa propriedade.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

</dd> <dt>

**MaxXResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A resolução máxima de X com suporte do servidor. Use o método [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) para modificar essa propriedade.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

</dd> <dt>

**MaxYResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A resolução de Y máxima com suporte no servidor. Use o método [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) para modificar essa propriedade.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PNPRedirection**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o redirecionamento de Plug and Play deve ser permitido.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Permitir redirecionamento de Plug and Play.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

Não permitir redirecionamento de Plug and Play.

</dd> </dl>

</dd> <dt>

**PolicyAdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **AdvancedRemoteAppGraphics** está configurada pelo servidor ou pela política de grupo.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2012 R2 e Windows 8.1.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceAllowDwm**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Esta propriedade não está disponível.

* * Windows 7 e Windows Server 2008 R2: * *

Indica se a propriedade **AllowDwm** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceAudioCaptureRedir**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **AudioCaptureRedir** está configurada pelo servidor ou pela política de grupo.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceAudioMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **AudioMapping** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como a propriedade **AVC444ModePreferredis** é configurada.

**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows Server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 10 ou do Windows Server 2016.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo

</dd> </dl>

</dd> <dt>

**PolicySourceClipboardMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **ClipboardMapping** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **ColorDepth** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepthPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **ColorDepthPolicy** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceCOMPortMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **COMPortMapping** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceDefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **DefaultToClientPrinter** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceDriveMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **DriveMapping** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceEncodeImageQuality**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como o **EncodeImageQualityi** é configurado.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo

</dd> </dl>

</dd> <dt>

**PolicySourceHardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como o **HardwareGraphicsAdapter** é configurado.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo

</dd> </dl>

</dd> <dt>

**PolicySourceLPTPortMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **LPTPortMapping** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceMaxMonitors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **MaxMonitors** está configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

</dd> <dt>

**PolicySourceMaxResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se as propriedades **MaxXResolution** e **MaxYResolution** são configuradas pelo servidor, pela política de grupo ou por padrão.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourcePNPRedirection**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **PNPRedirection** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceRemoteSessionProfile**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como o **RemoteSessionProfile** é configurado.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSelectNetworkDetect**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como a propriedade **SelectNetworkDetect** é configurada.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSelectTransport**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como a propriedade **SelectTransport** é configurada.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo

</dd> </dl>

</dd> <dt>

**PolicySourceVideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **VideoPlaybackRedir** está configurada pelo servidor ou pela política de grupo.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceWindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **WindowsPrinterMapping** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**RemoteSessionProfile**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica o perfil para a experiência de RDP.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**escala** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**experiência** (2)


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**largura de banda** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**SelectNetworkDetect**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se a detecção de rede é usada.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

usado no momento da conexão e no estado Steady.

</dd> <dt>

1
</dt> <dd>

desabilitado no momento da conexão

</dd> <dt>

2
</dt> <dd>

desabilitado no estado estável

</dd> <dt>

3
</dt> <dd>

desabilitado no momento da conexão e no estado Steady.

</dd> </dl>

</dd> <dt>

**SelectTransport**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica quais protocolos de transporte podem ser usados para acesso de RDP ao servidor.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.

<dt>

0
</dt> <dd>

Use UDP e TCP.

</dd> <dt>

1
</dt> <dd>

Use somente TCP.

</dd> <dt>

2
</dt> <dd>

Use UDP ou TCP.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Erro")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconhecido")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Parando")


</dt> <dd></dd> <dt>



 ("Serviço")


</dt> <dd></dd> </dl>

</dd> <dt>

**Terminalname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do terminal.

Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**VideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o redirecionamento de reprodução de vídeo deve ser permitido.

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**Verdadeiro** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o mapeamento de impressora está desabilitado ou habilitado para a janela do cliente.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O mapeamento de impressora está habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O mapeamento de impressora está desabilitado.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

Lembre-se de que uma estação de janela associada à sessão de console não pode acessar os métodos e as propriedades dessa classe. Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade **terminalname** , os métodos desse objeto retornarão o **WBEM \_ E não \_ terão \_ suporte**. Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.

Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de seis.

O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Terminal do Win32 \_**](win32-terminal.md)
</dt> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dt>

[**Configuração de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

