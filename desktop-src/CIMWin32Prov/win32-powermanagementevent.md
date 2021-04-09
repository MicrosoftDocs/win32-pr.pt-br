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
# <a name="win32_powermanagementevent-class"></a>\_Classe Win32 PowerManagementEvent

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent do Win32** representa eventos de gerenciamento de energia resultantes de alterações de estado de energia. Essas alterações de estado são associadas ao APM (gerenciamento avançado de energia) ou aos protocolos de gerenciamento de sistema da interface de energia e configuração avançada (ACPI).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Win32 \_ PowerManagementEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PowerManagementEvent** tem essas propriedades.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| eventos de gerenciamento de energia")
</dt> </dl>

Tipo de alteração no estado de energia do sistema.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Inserindo suspensão** (4)


</dt> <dd>

Enquanto estiver suspenso, o computador parece estar desativado; no entanto, ele pode ser "ativado" em resposta a vários eventos, incluindo a entrada do usuário (como mover o mouse ou pressionar uma tecla no teclado). Enquanto o computador está suspenso, o consumo de energia é reduzido para um dos vários níveis, dependendo de como o sistema deve ser usado. Quanto menor o nível de consumo de energia, mais tempo leva o sistema para retornar ao estado de trabalho. Quando o computador entra no estado suspender, a área de trabalho está bloqueada e você deve pressionar CTRL + ALT + DELETE e fornecer um nome de usuário e senha válidos para retomar as operações

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Retomar da suspensão** (7)


</dt> <dd>

Indica que um reinício da mensagem de suspensão foi enviado, permitindo que o computador retorne ao seu estado de energia normal.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Alteração do status de energia** (10)


</dt> <dd>

Indica uma alteração no status de energia do computador, como uma mudança de energia da bateria para AC ou de AC para uma fonte de alimentação ininterrupta. O sistema também transmite esse evento quando a energia restante da bateria fica abaixo do limite especificado pelo usuário ou se a energia da bateria for alterada em um percentual especificado.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento OEM** (11)


</dt> <dd>

Indica que um BIOS de gerenciamento avançado de energia (APM) enviou um evento OEM. O valor do evento será capturado na propriedade **OEMEventCode** . Como algumas implementações do BIOS do APM não fornecem notificações de eventos do OEM, esse evento pode nunca ser transmitido em alguns computadores. O APM é um esquema de gerenciamento de energia herdado. Embora ainda tenha suporte, o APM foi amplamente substituído pela ACPI (interface de energia e configuração avançada).

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Retomar automático** (18)


</dt> <dd>

Indica que o computador foi ativado em resposta a um evento. Se o sistema detectar a atividade do usuário (como um clique do mouse), a mensagem ResumeSuspend será transmitida, permitindo que os aplicativos saibam que eles podem retomar a interatividade completa com o usuário.

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| eventos de gerenciamento de energia")
</dt> </dl>

Estado de energia do sistema definido pelo OEM (fabricante original do equipamento) quando a propriedade **EventType** dessa classe é definida como 11 (evento OEM); caso contrário, essa propriedade será definida como **NULL**. Os eventos OEM são gerados quando um BIOS do APM sinaliza um evento de OEM do APM. Os códigos de evento OEM estão no intervalo 0x0200h-0x02FFh.

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado).

Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PowerManagementEvent** é derivada de [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).

As alterações no status de energia geralmente indicam que um problema ocorreu com um computador ou com outro dispositivo gerenciado. Se um servidor muda repentinamente de energia AC para uma fonte de energia ininterrupta, essa alteração pode indicar que um problema elétrico de algum tipo ocorreu, seja com o próprio computador ou com o sistema elétrico na sala em que o computador é mantido.

Os administradores precisam monitorar essas alterações no status de energia e ser notificado sobre essas alterações imediatamente. Isso permite que eles tomem medidas antes que o dispositivo perca totalmente a energia. (Os sistemas de fonte de energia ininterrupta, por exemplo, podem ser executados por apenas 15 minutos ou mais antes de desligar.)

A classe **Win32 \_ PowerManagementEvent** pode ser usada para monitorar alterações no status de energia em um computador. Essas alterações podem incluir uma mudança de uma fonte de alimentação para outra, bem como uma alteração no estado de energia do computador (por exemplo, entrando ou saindo do modo de suspensão).

A classe **Win32 \_ PowerManagementEvent** tem apenas duas propriedades: EventType, usada para indicar o tipo de evento de alteração de energia que ocorreu e OEMEventType, que é usado por alguns fabricantes de equipamentos originais para definir eventos de alteração de energia adicionais.

Para obter mais informações sobre como responder a eventos de energia do Windows, consulte o artigo [monitorar e responder a eventos de energia do Windows com o PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) no Ei! Equipe de scripts! blog.

## <a name="examples"></a>Exemplos

O VBScript a seguir monitora as alterações no status de energia em um computador.


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



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

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[Monitorando alterações no status de energia do computador](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
