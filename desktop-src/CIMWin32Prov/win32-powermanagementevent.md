---
description: O Win32 \_ PowerManagementEvent &\# 32; A classe WMI representa os eventos de gerenciamento de energia resultantes de alterações de estado de energia.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Classe Win32_PowerManagementEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089218"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="45cbc-103">\_Classe Win32 PowerManagementEvent</span><span class="sxs-lookup"><span data-stu-id="45cbc-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="45cbc-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent do Win32** representa eventos de gerenciamento de energia resultantes de alterações de estado de energia.</span><span class="sxs-lookup"><span data-stu-id="45cbc-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="45cbc-105">Essas alterações de estado são associadas ao APM (gerenciamento avançado de energia) ou aos protocolos de gerenciamento de sistema da interface de energia e configuração avançada (ACPI).</span><span class="sxs-lookup"><span data-stu-id="45cbc-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="45cbc-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="45cbc-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="45cbc-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="45cbc-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cbc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45cbc-108">Syntax</span></span>

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a><span data-ttu-id="45cbc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="45cbc-109">Members</span></span>

<span data-ttu-id="45cbc-110">A classe **Win32 \_ PowerManagementEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="45cbc-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="45cbc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="45cbc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45cbc-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="45cbc-112">Properties</span></span>

<span data-ttu-id="45cbc-113">A classe **Win32 \_ PowerManagementEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="45cbc-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45cbc-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="45cbc-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cbc-115">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cbc-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cbc-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45cbc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cbc-117">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| eventos de gerenciamento de energia")</span><span class="sxs-lookup"><span data-stu-id="45cbc-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="45cbc-118">Tipo de alteração no estado de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="45cbc-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="45cbc-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Inserindo suspensão** (4)</span><span class="sxs-lookup"><span data-stu-id="45cbc-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="45cbc-120">Enquanto estiver suspenso, o computador parece estar desativado; no entanto, ele pode ser "ativado" em resposta a vários eventos, incluindo a entrada do usuário (como mover o mouse ou pressionar uma tecla no teclado).</span><span class="sxs-lookup"><span data-stu-id="45cbc-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="45cbc-121">Enquanto o computador está suspenso, o consumo de energia é reduzido para um dos vários níveis, dependendo de como o sistema deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="45cbc-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="45cbc-122">Quanto menor o nível de consumo de energia, mais tempo leva o sistema para retornar ao estado de trabalho.</span><span class="sxs-lookup"><span data-stu-id="45cbc-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="45cbc-123">Quando o computador entra no estado suspender, a área de trabalho está bloqueada e você deve pressionar CTRL + ALT + DELETE e fornecer um nome de usuário e senha válidos para retomar as operações</span><span class="sxs-lookup"><span data-stu-id="45cbc-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="45cbc-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Retomar da suspensão** (7)</span><span class="sxs-lookup"><span data-stu-id="45cbc-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="45cbc-125">Indica que um reinício da mensagem de suspensão foi enviado, permitindo que o computador retorne ao seu estado de energia normal.</span><span class="sxs-lookup"><span data-stu-id="45cbc-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="45cbc-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Alteração do status de energia** (10)</span><span class="sxs-lookup"><span data-stu-id="45cbc-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="45cbc-127">Indica uma alteração no status de energia do computador, como uma mudança de energia da bateria para AC ou de AC para uma fonte de alimentação ininterrupta.</span><span class="sxs-lookup"><span data-stu-id="45cbc-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="45cbc-128">O sistema também transmite esse evento quando a energia restante da bateria fica abaixo do limite especificado pelo usuário ou se a energia da bateria for alterada em um percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="45cbc-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="45cbc-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento OEM** (11)</span><span class="sxs-lookup"><span data-stu-id="45cbc-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="45cbc-130">Indica que um BIOS de gerenciamento avançado de energia (APM) enviou um evento OEM.</span><span class="sxs-lookup"><span data-stu-id="45cbc-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="45cbc-131">O valor do evento será capturado na propriedade **OEMEventCode** .</span><span class="sxs-lookup"><span data-stu-id="45cbc-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="45cbc-132">Como algumas implementações do BIOS do APM não fornecem notificações de eventos do OEM, esse evento pode nunca ser transmitido em alguns computadores.</span><span class="sxs-lookup"><span data-stu-id="45cbc-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="45cbc-133">O APM é um esquema de gerenciamento de energia herdado.</span><span class="sxs-lookup"><span data-stu-id="45cbc-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="45cbc-134">Embora ainda tenha suporte, o APM foi amplamente substituído pela ACPI (interface de energia e configuração avançada).</span><span class="sxs-lookup"><span data-stu-id="45cbc-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="45cbc-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Retomar automático** (18)</span><span class="sxs-lookup"><span data-stu-id="45cbc-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="45cbc-136">Indica que o computador foi ativado em resposta a um evento.</span><span class="sxs-lookup"><span data-stu-id="45cbc-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="45cbc-137">Se o sistema detectar a atividade do usuário (como um clique do mouse), a mensagem ResumeSuspend será transmitida, permitindo que os aplicativos saibam que eles podem retomar a interatividade completa com o usuário.</span><span class="sxs-lookup"><span data-stu-id="45cbc-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45cbc-138">**OEMEventCode**</span><span class="sxs-lookup"><span data-stu-id="45cbc-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cbc-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cbc-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cbc-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45cbc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cbc-141">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| eventos de gerenciamento de energia")</span><span class="sxs-lookup"><span data-stu-id="45cbc-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="45cbc-142">Estado de energia do sistema definido pelo OEM (fabricante original do equipamento) quando a propriedade **EventType** dessa classe é definida como 11 (evento OEM); caso contrário, essa propriedade será definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="45cbc-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="45cbc-143">Os eventos OEM são gerados quando um BIOS do APM sinaliza um evento de OEM do APM.</span><span class="sxs-lookup"><span data-stu-id="45cbc-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="45cbc-144">Os códigos de evento OEM estão no intervalo 0x0200h-0x02FFh.</span><span class="sxs-lookup"><span data-stu-id="45cbc-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="45cbc-145">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="45cbc-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cbc-146">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="45cbc-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="45cbc-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45cbc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cbc-148">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="45cbc-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="45cbc-149">Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="45cbc-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="45cbc-150">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="45cbc-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="45cbc-151">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="45cbc-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cbc-152">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cbc-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cbc-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45cbc-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cbc-154">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="45cbc-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="45cbc-155">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="45cbc-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="45cbc-156">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="45cbc-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="45cbc-157">Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="45cbc-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="45cbc-158">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="45cbc-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45cbc-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="45cbc-159">Remarks</span></span>

<span data-ttu-id="45cbc-160">A classe **Win32 \_ PowerManagementEvent** é derivada de [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="45cbc-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="45cbc-161">As alterações no status de energia geralmente indicam que um problema ocorreu com um computador ou com outro dispositivo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="45cbc-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="45cbc-162">Se um servidor muda repentinamente de energia AC para uma fonte de energia ininterrupta, essa alteração pode indicar que um problema elétrico de algum tipo ocorreu, seja com o próprio computador ou com o sistema elétrico na sala em que o computador é mantido.</span><span class="sxs-lookup"><span data-stu-id="45cbc-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="45cbc-163">Os administradores precisam monitorar essas alterações no status de energia e ser notificado sobre essas alterações imediatamente.</span><span class="sxs-lookup"><span data-stu-id="45cbc-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="45cbc-164">Isso permite que eles tomem medidas antes que o dispositivo perca totalmente a energia.</span><span class="sxs-lookup"><span data-stu-id="45cbc-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="45cbc-165">(Os sistemas de fonte de energia ininterrupta, por exemplo, podem ser executados por apenas 15 minutos ou mais antes de desligar.)</span><span class="sxs-lookup"><span data-stu-id="45cbc-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="45cbc-166">A classe **Win32 \_ PowerManagementEvent** pode ser usada para monitorar alterações no status de energia em um computador.</span><span class="sxs-lookup"><span data-stu-id="45cbc-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="45cbc-167">Essas alterações podem incluir uma mudança de uma fonte de alimentação para outra, bem como uma alteração no estado de energia do computador (por exemplo, entrando ou saindo do modo de suspensão).</span><span class="sxs-lookup"><span data-stu-id="45cbc-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="45cbc-168">A classe **Win32 \_ PowerManagementEvent** tem apenas duas propriedades: EventType, usada para indicar o tipo de evento de alteração de energia que ocorreu e OEMEventType, que é usado por alguns fabricantes de equipamentos originais para definir eventos de alteração de energia adicionais.</span><span class="sxs-lookup"><span data-stu-id="45cbc-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="45cbc-169">Para obter mais informações sobre como responder a eventos de energia do Windows, consulte o artigo [monitorar e responder a eventos de energia do Windows com o PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) no Ei!</span><span class="sxs-lookup"><span data-stu-id="45cbc-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="45cbc-170">Equipe de scripts!</span><span class="sxs-lookup"><span data-stu-id="45cbc-170">Scripting Guy!</span></span> <span data-ttu-id="45cbc-171">blog.</span><span class="sxs-lookup"><span data-stu-id="45cbc-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="45cbc-172">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45cbc-172">Examples</span></span>

<span data-ttu-id="45cbc-173">O VBScript a seguir monitora as alterações no status de energia em um computador.</span><span class="sxs-lookup"><span data-stu-id="45cbc-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="45cbc-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45cbc-174">Requirements</span></span>



| <span data-ttu-id="45cbc-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="45cbc-175">Requirement</span></span> | <span data-ttu-id="45cbc-176">Valor</span><span class="sxs-lookup"><span data-stu-id="45cbc-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45cbc-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45cbc-177">Minimum supported client</span></span><br/> | <span data-ttu-id="45cbc-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45cbc-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45cbc-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45cbc-179">Minimum supported server</span></span><br/> | <span data-ttu-id="45cbc-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45cbc-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45cbc-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="45cbc-181">Namespace</span></span><br/>                | <span data-ttu-id="45cbc-182">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="45cbc-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45cbc-183">MOF</span><span class="sxs-lookup"><span data-stu-id="45cbc-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45cbc-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45cbc-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45cbc-185">DLL</span><span class="sxs-lookup"><span data-stu-id="45cbc-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45cbc-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45cbc-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45cbc-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="45cbc-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cbc-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="45cbc-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="45cbc-189">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="45cbc-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="45cbc-190">[Monitorando alterações no status de energia do computador](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="45cbc-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
