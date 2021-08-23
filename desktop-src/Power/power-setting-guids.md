---
description: GUIDs de configuração de energia identificam eventos de alteração de energia.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUIDs de configuração de energia (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b05909509e0c3ed581582ebe90b10e5df4e91a31b7ab050b3fd1ef6679b1a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887026"
---
# <a name="power-setting-guids"></a>GUIDs de configuração de energia

A configuração de energia **GUID** s identifica eventos de alteração de energia. Este tópico lista as configurações de energia **GUID** s para notificações que são mais úteis para os aplicativos. Um aplicativo deve se registrar para cada evento de alteração de energia que possa afetar seu comportamento. A notificação é enviada cada vez que uma configuração é alterada.

As configurações de energia **GUID** s são definidas em Winnt. h.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**fonte de energia do GUID \_ ACDC \_ \_**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



A fonte de energia do sistema foi alterada. O membro de **dados** é um **DWORD** com valores da enumeração de [**\_ \_ condição de energia do sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) que indica a fonte de energia atual.

<dl> <dt>

**PoAc** (0)-o computador é alimentado por uma fonte de energia CA (ou semelhante, como um laptop alimentado por um adaptador automotivo de 12V).
</dt> <dt>

**PoDc** (1)-o computador é alimentado por uma fonte de energia de bateria integrada.
</dt> <dt>

**PoHot** (2)-o computador é alimentado por uma fonte de energia de curto prazo, como um dispositivo UPS.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**porcentagem de bateria de GUID \_ \_ \_ restante**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



A capacidade restante da bateria foi alterada. A granularidade varia de sistema para sistema, mas a granularidade mais fina é 1%. O membro de **dados** é um **DWORD** que indica a capacidade da bateria atual restante como uma porcentagem de 0 a 100.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_estado de \_ exibição do console GUID \_**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



O estado de exibição do monitor atual foi alterado.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** essa notificação está disponível a partir de Windows 8 e Windows Server 2012.

O membro de **dados** é um **DWORD** com um dos valores a seguir.

<dl> <dt>

0x0-a exibição está desativada.
</dt> <dt>

0x1-a exibição está ativada.
</dt> <dt>

0x2-a exibição está esmaecida.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_presença do \_ usuário \_ global do GUID**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



O status do usuário associado a qualquer sessão foi alterado. Isso representa o status combinado da presença do usuário em todas as sessões locais e remotas no sistema.

Essa notificação é enviada somente para serviços e outros programas em execução na sessão 0. Os aplicativos de modo de usuário devem se registrar para a **\_ presença de \_ usuário \_ de sessão GUID** em vez disso.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** essa notificação está disponível a partir de Windows 8 e Windows Server 2012.

O membro de **dados** é um **DWORD** com um dos valores a seguir.

<dl> <dt>

**PowerUserPresent** (0)-o usuário está presente em qualquer sessão local ou remota no sistema.
</dt> <dt>

**PowerUserInactive** (2)-o usuário não está presente em nenhuma sessão local ou remota no sistema.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_tarefa de \_ segundo plano de ociosidade do GUID \_**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



O sistema está ocupado. Isso indica que o sistema não estará mudando para um estado ocioso em um futuro próximo e que a hora atual é um bom momento para que os componentes executem tarefas de segundo plano ou ociosas que, de outra forma, impediriam que o computador entrasse em um estado ocioso.

Não há nenhuma notificação quando o sistema é capaz de passar para um estado ocioso. A notificação de tarefa de segundo plano ociosa não indica se um usuário está presente no computador. O membro de **dados** não tem informações e pode ser ignorado.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ ativação do monitor \_ de GUID**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



O monitor do sistema primário foi ligado ou desligado. Essa notificação é útil para componentes que processam ativamente o conteúdo para o dispositivo de vídeo, como a visualização de mídia. Esses aplicativos devem se registrar para essa notificação e parar de renderizar o conteúdo de gráficos quando o monitor estiver desativado para reduzir o consumo de energia do sistema. O membro de **dados** é um **DWORD** que indica o estado atual do monitor.

<dl> <dt>

0x0-o monitor está desativado.
</dt> <dt>

0x1-o monitor está ativado.
</dt> </dl>

**Windows 8 e Windows Server 2012:** Os novos aplicativos devem usar o **\_ estado de \_ exibição \_ do console GUID** em vez desta notificação.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_status de \_ economia de energia do GUID \_**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



A economia de bateria foi desativada ou ativada em resposta à alteração das condições de energia. Essa notificação é útil para os componentes que participam da conservação de energia. Esses aplicativos devem se registrar para essa notificação e economizar energia quando a economia de bateria estiver ativada.

O membro de **dados** é um **DWORD** que indica o estado de economia de bateria.

<dl> <dt>

0x0-a economia de bateria está desativada.
</dt> <dt>

0x1-a economia de bateria está ativada. Economize energia sempre que possível.
</dt> </dl>

Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_personalidade POWERSCHEME do GUID \_**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



A personalidade do esquema de energia ativo foi alterada. Todos os esquemas de energia são mapeados para um desses personalidades. O membro de **dados** é um **GUID** que indica a nova personalidade de esquema de energia ativo.

<dl> <dt>



**GUID \_ do \_ \_ Economia mínima de energia** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)

Alto desempenho-o esquema foi projetado para oferecer o desempenho máximo às custas da economia de consumo de energia.


</dt> <dt>



**GUID \_ do \_ \_ Economia máxima de energia** (A1841308-3541-4FAB-BC81-F71556F20B4A)

Economia de energia – o esquema foi projetado para oferecer economia de consumo de energia máxima às custas do desempenho e da capacidade de resposta do sistema.


</dt> <dt>



**GUID \_ do \_ \_ Economia de energia típica** (381B4222-F694-41F0-9685-FF5BB260DF2E)

Automático-o esquema foi projetado para balancear automaticamente o desempenho e a economia de consumo de energia.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_status de \_ exibição da sessão GUID \_**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



A exibição associada à sessão do aplicativo foi ligada ou desativada.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** essa notificação está disponível a partir de Windows 8 e Windows Server 2012.

Essa notificação é enviada somente para aplicativos de modo de usuário. Os serviços e outros programas em execução na sessão 0 não recebem essa notificação. O membro de **dados** é um **DWORD** com um dos valores a seguir.

<dl> <dt>

0x0-a exibição está desativada.
</dt> <dt>

0x1-a exibição está ativada.
</dt> <dt>

0x2-a exibição está esmaecida.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_presença de \_ usuário de sessão GUID \_**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



O status do usuário associado à sessão do aplicativo foi alterado.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** essa notificação está disponível a partir de Windows 8 e Windows Server 2012.

Essa notificação é enviada somente para aplicativos de modo de usuário em execução em uma sessão interativa. Os serviços e outros programas em execução na sessão 0 devem ser registrados para a **\_ \_ \_ presença do usuário global do GUID**. O membro de **dados** é um **DWORD** com um dos valores a seguir.

<dl> <dt>

**PowerUserPresent** (0)-o usuário está fornecendo entrada para a sessão.
</dt> <dt>

**PowerUserInactive** (2)-o tempo limite da atividade do usuário expirou sem interação do usuário.
</dt> </dl>

> [!Note]  
> Todos os aplicativos executados em uma sessão de modo de usuário interativo devem usar essa configuração. Quando os aplicativos de modo kernel se registram para o status do monitor, eles devem usar o **\_ status de \_ exibição \_ do console GUID** .

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**sistema do GUID \_ \_ ausentemode**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



O sistema está entrando ou saindo do modo ausente. O membro de **dados** é um **DWORD** que indica o estado atual do modo ausente.

<dl> <dt>

0x0-o computador está saindo do modo ausente.
</dt> <dt>

0x1-o computador está entrando no modo ausente.
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WinNT. h</dt> </dl> |



 

