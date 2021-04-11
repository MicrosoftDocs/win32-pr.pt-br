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
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="89111-105">\_Classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="89111-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="89111-106">A classe WMI **\_ TSClientSetting do Win32** define as definições de configuração para a classe de [**\_ terminal Win32**](win32-terminal.md) relacionada à política de conexão.</span><span class="sxs-lookup"><span data-stu-id="89111-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="89111-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="89111-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="89111-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="89111-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="89111-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89111-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="89111-110">Membros</span><span class="sxs-lookup"><span data-stu-id="89111-110">Members</span></span>

<span data-ttu-id="89111-111">A classe **Win32 \_ TSClientSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89111-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="89111-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="89111-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="89111-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89111-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="89111-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="89111-114">Methods</span></span>

<span data-ttu-id="89111-115">A classe **Win32 \_ TSClientSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="89111-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="89111-116">Método</span><span class="sxs-lookup"><span data-stu-id="89111-116">Method</span></span>                                                                   | <span data-ttu-id="89111-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="89111-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89111-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="89111-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="89111-119">Define as propriedades **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** e **DefaultToClientPrinter** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="89111-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="89111-120">**SetAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="89111-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="89111-121">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="89111-121">Not supported.</span></span><br/> <span data-ttu-id="89111-122">**Windows 7 e Windows Server 2008 R2:** Define a propriedade **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="89111-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="89111-123">**Setclientproperty**</span><span class="sxs-lookup"><span data-stu-id="89111-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="89111-124">Define a propriedade **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="89111-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="89111-125">**SetColorDepth**</span><span class="sxs-lookup"><span data-stu-id="89111-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="89111-126">Define a propriedade **ColorDepth** .</span><span class="sxs-lookup"><span data-stu-id="89111-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="89111-127">**SetColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="89111-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="89111-128">Define a propriedade **ColorDepthPolicy** .</span><span class="sxs-lookup"><span data-stu-id="89111-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="89111-129">**SetMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="89111-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="89111-130">Define a propriedade **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="89111-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="89111-131">**SetMaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="89111-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="89111-132">Define a propriedade **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="89111-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="89111-133">**SetMaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="89111-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="89111-134">Define a propriedade **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="89111-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="89111-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89111-135">Properties</span></span>

<span data-ttu-id="89111-136">A classe **Win32 \_ TSClientSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89111-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89111-137">**AdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="89111-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-140">Especifica se é para habilitar gráficos RemoteFX avançados para o RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="89111-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="89111-141">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2012 R2 e Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="89111-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-142"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-143">Os gráficos avançados estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="89111-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-144"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-145">Os gráficos avançados estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="89111-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-146">**AllowDwm**</span><span class="sxs-lookup"><span data-stu-id="89111-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-149">Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="89111-149">This property is not available.</span></span>

<span data-ttu-id="89111-150">\* \* Windows 7 e Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="89111-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="89111-151">Especifica se a composição da área de trabalho remota deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="89111-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="89111-152">Zero desabilitará a composição de área de trabalho remota e um valor diferente de zero permitirá isso.</span><span class="sxs-lookup"><span data-stu-id="89111-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="89111-153">Use o método [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) para modificar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="89111-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="89111-154">**AudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="89111-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-157">Especifica se o redirecionamento de captura de áudio deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="89111-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="89111-158">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-159">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-160">**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-161">**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-164">Especifica se o mapeamento de áudio está desabilitado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-165"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-166">O mapeamento de áudio está habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-167"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-168">O mapeamento de áudio está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="89111-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-171">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-172">Especifica se o modo AVC444 é preferencial.</span><span class="sxs-lookup"><span data-stu-id="89111-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="89111-173">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows Server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 10 ou do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="89111-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-174">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-175">**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-176">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="89111-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89111-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89111-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89111-179">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="89111-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="89111-180">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="89111-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="89111-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89111-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89111-182">**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-185">Especifica se o mapeamento da área de transferência está desabilitado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-186"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-187">O mapeamento da área de transferência está habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-188"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-189">O mapeamento da área de transferência está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-190">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="89111-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-191">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-193">Especifica a profundidade de cor.</span><span class="sxs-lookup"><span data-stu-id="89111-193">Specifies the color depth.</span></span> <span data-ttu-id="89111-194">Para obter os valores possíveis, consulte o método [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .</span><span class="sxs-lookup"><span data-stu-id="89111-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="89111-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bits** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="89111-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bits** (2)</span><span class="sxs-lookup"><span data-stu-id="89111-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="89111-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bits** (3)</span><span class="sxs-lookup"><span data-stu-id="89111-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="89111-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bits** (4)</span><span class="sxs-lookup"><span data-stu-id="89111-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="89111-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bits** (5)</span><span class="sxs-lookup"><span data-stu-id="89111-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-200">**ColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="89111-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-203">Especifica se a configuração de cor máxima do usuário deve ser substituída.</span><span class="sxs-lookup"><span data-stu-id="89111-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-204"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-205">Não substitua a política do usuário.</span><span class="sxs-lookup"><span data-stu-id="89111-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-206"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-207">Substituir a política do usuário.</span><span class="sxs-lookup"><span data-stu-id="89111-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-208">**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-209">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-211">Especifica se o mapeamento de porta COM está desabilitado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-212"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-213">O mapeamento de porta COM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-214"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-215">O mapeamento de porta COM está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-216">**ConnectClientDrivesAtLogon**</span><span class="sxs-lookup"><span data-stu-id="89111-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-217">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-219">Especifica se as unidades do cliente serão conectadas automaticamente durante o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="89111-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-220"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-221">As unidades não serão conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="89111-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-222"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-223">As unidades serão conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="89111-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="89111-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-225">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-227">A política que o servidor usa para recuperar as configurações de conexão do usuário.</span><span class="sxs-lookup"><span data-stu-id="89111-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="89111-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-229">As configurações de conexão do usuário estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="89111-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="89111-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-231">As configurações de conexão do usuário são substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="89111-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-232">**ConnectPrinterAtLogon**</span><span class="sxs-lookup"><span data-stu-id="89111-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-233">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-235">Especifica se todas as impressoras locais mapeadas do cliente serão conectadas automaticamente durante o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="89111-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-236"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-237">As impressoras locais não serão conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="89111-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-238"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-239">As impressoras locais serão conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="89111-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-240">**DefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="89111-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-241">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-243">Especifica se os trabalhos de impressão serão enviados automaticamente para a impressora local do cliente.</span><span class="sxs-lookup"><span data-stu-id="89111-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-244"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-245">Os trabalhos de impressão não devem ser enviados automaticamente para a impressora local do cliente.</span><span class="sxs-lookup"><span data-stu-id="89111-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-246"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-247">Os trabalhos de impressão devem ser enviados automaticamente para a impressora local do cliente.</span><span class="sxs-lookup"><span data-stu-id="89111-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-248">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="89111-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89111-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89111-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-251">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="89111-251">Description of the object.</span></span>

<span data-ttu-id="89111-252">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89111-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89111-253">**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-254">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-256">Especifica se o mapeamento de unidade está desabilitado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-257"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-258">O mapeamento de unidade está habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-259"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-260">O mapeamento de unidade está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-261">**EncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="89111-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-263">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-264">Especifica a qualidade da imagem para a experiência RDP.</span><span class="sxs-lookup"><span data-stu-id="89111-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="89111-265">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="89111-266">**sem perdas** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="89111-267">**alta** (2)</span><span class="sxs-lookup"><span data-stu-id="89111-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="89111-268">**médio** (3)</span><span class="sxs-lookup"><span data-stu-id="89111-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-269">**HardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="89111-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-270">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-272">Especifica se o servidor de Host da Sessão RD usa o processador de gráficos de hardware como o adaptador padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="89111-273">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-274">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-275">**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="89111-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-277">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="89111-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89111-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89111-279">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="89111-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="89111-280">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="89111-280">The date the object was installed.</span></span> <span data-ttu-id="89111-281">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="89111-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="89111-282">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89111-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89111-283">**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-284">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-286">Especifica se o mapeamento de porta LPT está desabilitado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-287"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-288">O mapeamento de porta LPT está habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-289"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-290">O mapeamento de porta LPT está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-291">**MaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="89111-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-292">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-294">O número máximo de monitores com suporte no servidor.</span><span class="sxs-lookup"><span data-stu-id="89111-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="89111-295">Use o método [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) para modificar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="89111-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="89111-296">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="89111-297">**MaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="89111-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-298">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-300">A resolução máxima de X com suporte do servidor.</span><span class="sxs-lookup"><span data-stu-id="89111-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="89111-301">Use o método [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) para modificar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="89111-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="89111-302">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="89111-303">**MaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="89111-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-304">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-306">A resolução de Y máxima com suporte no servidor.</span><span class="sxs-lookup"><span data-stu-id="89111-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="89111-307">Use o método [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) para modificar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="89111-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="89111-308">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="89111-309">**Nome**</span><span class="sxs-lookup"><span data-stu-id="89111-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89111-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89111-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-312">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="89111-312">The name of the object.</span></span>

<span data-ttu-id="89111-313">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89111-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89111-314">**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="89111-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-315">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-317">Especifica se o redirecionamento de Plug and Play deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="89111-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-318"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-319">Permitir redirecionamento de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="89111-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-320"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-321">Não permitir redirecionamento de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="89111-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-322">**PolicyAdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="89111-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-323">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-325">Indica se a propriedade **AdvancedRemoteAppGraphics** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="89111-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="89111-326">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2012 R2 e Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="89111-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="89111-327">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-328">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-329">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-330">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-331">**PolicySourceAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="89111-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-332">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-334">Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="89111-334">This property is not available.</span></span>

<span data-ttu-id="89111-335">\* \* Windows 7 e Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="89111-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="89111-336">Indica se a propriedade **AllowDwm** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="89111-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="89111-337">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-338">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-339">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-340">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-341">**PolicySourceAudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="89111-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-342">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-344">Indica se a propriedade **AudioCaptureRedir** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="89111-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="89111-345">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="89111-346">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-347">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-348">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-349">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-350">**PolicySourceAudioMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-351">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-353">Indica se a propriedade **AudioMapping** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-354">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-355">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-356">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-357">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-358">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-359">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="89111-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-361">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-363">Indica como a propriedade **AVC444ModePreferredis** é configurada.</span><span class="sxs-lookup"><span data-stu-id="89111-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="89111-364">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows Server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 10 ou do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="89111-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="89111-365">0</span><span class="sxs-lookup"><span data-stu-id="89111-365">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-366">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-367">1</span><span class="sxs-lookup"><span data-stu-id="89111-367">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-368">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="89111-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-369">**PolicySourceClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-370">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-372">Indica se a propriedade **ClipboardMapping** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-373">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-374">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-375">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-376">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-377">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-378">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-379">**PolicySourceColorDepth**</span><span class="sxs-lookup"><span data-stu-id="89111-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-380">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-382">Indica se a propriedade **ColorDepth** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-383">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-384">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-385">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-386">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-387">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-388">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-389">**PolicySourceColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="89111-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-390">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-392">Indica se a propriedade **ColorDepthPolicy** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-393">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-394">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-395">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-396">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-397">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-398">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-399">**PolicySourceCOMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-400">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-402">Indica se a propriedade **COMPortMapping** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-403">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-404">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-405">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-406">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-407">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-408">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-409">**PolicySourceDefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="89111-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-410">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-412">Indica se a propriedade **DefaultToClientPrinter** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-413">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-414">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-415">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-416">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-417">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-418">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-419">**PolicySourceDriveMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-420">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-422">Indica se a propriedade **DriveMapping** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-424">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-426">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-427">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-428">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-429">**PolicySourceEncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="89111-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-430">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-432">Indica como o **EncodeImageQualityi** é configurado.</span><span class="sxs-lookup"><span data-stu-id="89111-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="89111-433">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-434">0</span><span class="sxs-lookup"><span data-stu-id="89111-434">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-435">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-436">1</span><span class="sxs-lookup"><span data-stu-id="89111-436">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-437">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="89111-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-438">**PolicySourceHardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="89111-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-439">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-441">Indica como o **HardwareGraphicsAdapter** é configurado.</span><span class="sxs-lookup"><span data-stu-id="89111-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="89111-442">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-443">0</span><span class="sxs-lookup"><span data-stu-id="89111-443">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-444">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-445">1</span><span class="sxs-lookup"><span data-stu-id="89111-445">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-446">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="89111-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-447">**PolicySourceLPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-448">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-450">Indica se a propriedade **LPTPortMapping** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-451">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-452">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-453">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-454">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-455">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-456">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-457">**PolicySourceMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="89111-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-458">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-460">Indica se a propriedade **MaxMonitors** está configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="89111-461">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-462">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-463">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-464">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-465">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-466">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="89111-467">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="89111-468">**PolicySourceMaxResolution**</span><span class="sxs-lookup"><span data-stu-id="89111-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-469">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-471">Indica se as propriedades **MaxXResolution** e **MaxYResolution** são configuradas pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="89111-472">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="89111-473">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-474">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-475">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-476">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-477">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-478">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-479">**PolicySourcePNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="89111-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-480">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-482">Indica se a propriedade **PNPRedirection** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="89111-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="89111-483">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-484">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-485">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-486">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-487">**PolicySourceRemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="89111-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-488">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-490">Indica como o **RemoteSessionProfile** é configurado.</span><span class="sxs-lookup"><span data-stu-id="89111-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="89111-491">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-492">0</span><span class="sxs-lookup"><span data-stu-id="89111-492">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-493">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-494">1</span><span class="sxs-lookup"><span data-stu-id="89111-494">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-495">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="89111-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-496">**PolicySourceSelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="89111-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-497">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-498">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-499">Indica como a propriedade **SelectNetworkDetect** é configurada.</span><span class="sxs-lookup"><span data-stu-id="89111-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="89111-500">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-501">0</span><span class="sxs-lookup"><span data-stu-id="89111-501">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-502">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-503">1</span><span class="sxs-lookup"><span data-stu-id="89111-503">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-504">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="89111-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-505">**PolicySourceSelectTransport**</span><span class="sxs-lookup"><span data-stu-id="89111-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-506">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-508">Indica como a propriedade **SelectTransport** é configurada.</span><span class="sxs-lookup"><span data-stu-id="89111-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="89111-509">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-510">0</span><span class="sxs-lookup"><span data-stu-id="89111-510">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-511">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-512">1</span><span class="sxs-lookup"><span data-stu-id="89111-512">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-513">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="89111-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-514">**PolicySourceVideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="89111-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-515">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-516">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-517">Indica se a propriedade **VideoPlaybackRedir** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="89111-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="89111-518">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="89111-519">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-520">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-521">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-522">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-523">**PolicySourceWindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-524">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-525">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-526">Indica se a propriedade **WindowsPrinterMapping** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="89111-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="89111-527">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="89111-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="89111-528">Servidor</span><span class="sxs-lookup"><span data-stu-id="89111-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="89111-529">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="89111-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="89111-530">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="89111-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="89111-531">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="89111-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="89111-532">Padrão</span><span class="sxs-lookup"><span data-stu-id="89111-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-533">**RemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="89111-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-534">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-535">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-536">Especifica o perfil para a experiência de RDP.</span><span class="sxs-lookup"><span data-stu-id="89111-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="89111-537">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="89111-538">**escala** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="89111-539">**experiência** (2)</span><span class="sxs-lookup"><span data-stu-id="89111-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="89111-540">**largura de banda** (3)</span><span class="sxs-lookup"><span data-stu-id="89111-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-541">**SelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="89111-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-542">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-543">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-544">Especifica se a detecção de rede é usada.</span><span class="sxs-lookup"><span data-stu-id="89111-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="89111-545">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-546">0</span><span class="sxs-lookup"><span data-stu-id="89111-546">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-547">usado no momento da conexão e no estado Steady.</span><span class="sxs-lookup"><span data-stu-id="89111-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="89111-548">1</span><span class="sxs-lookup"><span data-stu-id="89111-548">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-549">desabilitado no momento da conexão</span><span class="sxs-lookup"><span data-stu-id="89111-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="89111-550">2</span><span class="sxs-lookup"><span data-stu-id="89111-550">2</span></span>
</dt> <dd>

<span data-ttu-id="89111-551">desabilitado no estado estável</span><span class="sxs-lookup"><span data-stu-id="89111-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="89111-552">3</span><span class="sxs-lookup"><span data-stu-id="89111-552">3</span></span>
</dt> <dd>

<span data-ttu-id="89111-553">desabilitado no momento da conexão e no estado Steady.</span><span class="sxs-lookup"><span data-stu-id="89111-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-554">**SelectTransport**</span><span class="sxs-lookup"><span data-stu-id="89111-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-555">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-556">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89111-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89111-557">Especifica quais protocolos de transporte podem ser usados para acesso de RDP ao servidor.</span><span class="sxs-lookup"><span data-stu-id="89111-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="89111-558">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa propriedade não está disponível antes do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89111-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="89111-559">0</span><span class="sxs-lookup"><span data-stu-id="89111-559">0</span></span>
</dt> <dd>

<span data-ttu-id="89111-560">Use UDP e TCP.</span><span class="sxs-lookup"><span data-stu-id="89111-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="89111-561">1</span><span class="sxs-lookup"><span data-stu-id="89111-561">1</span></span>
</dt> <dd>

<span data-ttu-id="89111-562">Use somente TCP.</span><span class="sxs-lookup"><span data-stu-id="89111-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="89111-563">2</span><span class="sxs-lookup"><span data-stu-id="89111-563">2</span></span>
</dt> <dd>

<span data-ttu-id="89111-564">Use UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="89111-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-565">**Status**</span><span class="sxs-lookup"><span data-stu-id="89111-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-566">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89111-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89111-567">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89111-568">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="89111-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="89111-569">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="89111-569">Current status of the object.</span></span> <span data-ttu-id="89111-570">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="89111-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="89111-571">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="89111-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="89111-572">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="89111-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="89111-573">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="89111-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="89111-574">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="89111-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="89111-575">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89111-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="89111-576">("OK")</span><span class="sxs-lookup"><span data-stu-id="89111-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-577">("Erro")</span><span class="sxs-lookup"><span data-stu-id="89111-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-578">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="89111-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-579">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="89111-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-580">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="89111-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-581">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="89111-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-582">("Parando")</span><span class="sxs-lookup"><span data-stu-id="89111-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89111-583">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="89111-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-584">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="89111-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-585">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89111-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89111-586">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-587">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="89111-587">The name of the terminal.</span></span>

<span data-ttu-id="89111-588">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="89111-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="89111-589">**VideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="89111-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-590">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-591">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-592">Especifica se o redirecionamento de reprodução de vídeo deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="89111-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="89111-593">**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível antes do Windows Server 2008 R2 e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89111-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-594">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-595">**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89111-596">**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="89111-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89111-597">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89111-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89111-598">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89111-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89111-599">Especifica se o mapeamento de impressora está desabilitado ou habilitado para a janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="89111-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="89111-600"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="89111-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89111-601">O mapeamento de impressora está habilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="89111-602"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="89111-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89111-603">O mapeamento de impressora está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="89111-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89111-604">Comentários</span><span class="sxs-lookup"><span data-stu-id="89111-604">Remarks</span></span>

<span data-ttu-id="89111-605">Lembre-se de que uma estação de janela associada à sessão de console não pode acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="89111-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="89111-606">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade **terminalname** , os métodos desse objeto retornarão o **WBEM \_ E não \_ terão \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="89111-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="89111-607">Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="89111-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="89111-608">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="89111-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="89111-609">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="89111-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="89111-610">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de seis.</span><span class="sxs-lookup"><span data-stu-id="89111-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="89111-611">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="89111-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="89111-612">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="89111-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="89111-613">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="89111-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="89111-614">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="89111-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="89111-615">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="89111-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="89111-616">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89111-616">Requirements</span></span>



| <span data-ttu-id="89111-617">Requisito</span><span class="sxs-lookup"><span data-stu-id="89111-617">Requirement</span></span> | <span data-ttu-id="89111-618">Valor</span><span class="sxs-lookup"><span data-stu-id="89111-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89111-619">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89111-619">Minimum supported client</span></span><br/> | <span data-ttu-id="89111-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89111-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89111-621">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89111-621">Minimum supported server</span></span><br/> | <span data-ttu-id="89111-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89111-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89111-623">Namespace</span><span class="sxs-lookup"><span data-stu-id="89111-623">Namespace</span></span><br/>                | <span data-ttu-id="89111-624">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="89111-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="89111-625">MOF</span><span class="sxs-lookup"><span data-stu-id="89111-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89111-626"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89111-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="89111-627">DLL</span><span class="sxs-lookup"><span data-stu-id="89111-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89111-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89111-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89111-629">Confira também</span><span class="sxs-lookup"><span data-stu-id="89111-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89111-630">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="89111-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="89111-631">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="89111-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="89111-632">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="89111-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

