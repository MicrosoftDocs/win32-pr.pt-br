---
description: As \_ constantes do estado \_ do dispositivo xxx indicam o estado atual de um dispositivo de ponto de extremidade de áudio.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: Constantes de DEVICE_STATE_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646214"
---
# <a name="device_state_xxx-constants"></a>Constantes do estado do dispositivo \_ \_ xxx

As \_ constantes do estado \_ do dispositivo xxx indicam o estado atual de um dispositivo de ponto de extremidade de áudio.



| Constante/valor                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**Dispositivo \_ do ESTADO \_ ativo**</dt> <dt>0x00000001</dt> </dl>             | O dispositivo de ponto de extremidade de áudio está ativo. Ou seja, o adaptador de áudio que se conecta ao dispositivo de ponto de extremidade está presente e habilitado. Além disso, se o dispositivo de ponto de extremidade se conectar a uma tomada no adaptador, o dispositivo de ponto de extremidade será conectado.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**Dispositivo \_ do ESTADO \_ desabilitado**</dt> <dt>0x00000002</dt> </dl>       | O dispositivo de ponto de extremidade de áudio está desabilitado. O usuário desabilitou o dispositivo no painel de controle multimídia do Windows Mmsys.cpl. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**Dispositivo \_ do Estado não \_ presente**</dt> <dt>0x00000004</dt> </dl> | O dispositivo de ponto de extremidade de áudio não está presente porque o adaptador de áudio que se conecta ao dispositivo de ponto de extremidade foi removido do sistema ou o usuário desabilitou o dispositivo de adaptador no Gerenciador de Dispositivos.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**Dispositivo \_ do Estado de 0x00000008 \_ DESconectado**</dt> <dt></dt> </dl>    | O dispositivo de ponto de extremidade de áudio está desconectado. O adaptador de áudio que contém a tomada para o dispositivo de ponto de extremidade está presente e habilitado, mas o dispositivo de ponto de extremidade não está conectado à tomada. Somente um dispositivo com detecção de presença de Jack pode estar nesse estado. Para obter mais informações sobre a detecção de presença de Jack, consulte [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**Dispositivo \_ do STATEMASK \_ todos os**</dt> <dt>0x0000000F</dt> </dl>          | Inclui dispositivos de ponto de extremidade de áudio em todos os Estados ativos, desabilitados, não presentes e desconectados.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Comentários

Os métodos [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)e [**IMMNotificationClient:: OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) usam as constantes do \_ estado do dispositivo \_ xxx. Esses métodos permitem que os clientes obtenham informações sobre dispositivos de ponto de extremidade que estão em qualquer um dos Estados representados pelas constantes do estado do dispositivo \_ \_ xxx.

No entanto, um cliente pode abrir um fluxo (por exemplo, obtendo uma interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para o dispositivo) somente em um dispositivo que esteja no \_ estado ativo do estado do dispositivo \_ .

O painel de controle multimídia do Windows, Mmsys.cpl, exibe os dispositivos de ponto de extremidade de áudio no sistema. A desabilitação de um dispositivo no Mmsys.cpl oculta o dispositivo dos mecanismos de descoberta de dispositivo em APIs de áudio de nível superior, mas não invalida os objetos de fluxo que um cliente pode ter instanciado antes de o dispositivo ser desabilitado. Por exemplo, se um fluxo estiver sendo reproduzido no dispositivo quando o usuário o desabilitar no Mmsys.cpl, o fluxo continuará a ser executado sem interrupções.

Por outro lado, desabilitar um dispositivo no Gerenciador de Dispositivos remove efetivamente o dispositivo do sistema.

Para usar Mmsys.cpl para exibir os dispositivos de renderização, abra uma janela de prompt de comando e digite o seguinte comando:

**controle mmsys.cpl,, 0**

Para exibir os dispositivos de captura, digite o seguinte comando:

**controle mmsys.cpl,, 1**

Como alternativa, você pode exibir os dispositivos de renderização ou os dispositivos de captura no Mmsys.cpl clicando com o botão direito do mouse no ícone de alto-falante na área de notificação, que está localizada no lado direito da barra de tarefas e selecionando **dispositivos de reprodução** ou de **gravação**.

Mmsys.cpl sempre exibe os dispositivos de ponto de extremidade que estão no \_ estado ativo do estado do dispositivo \_ . Além disso, ele pode ser configurado para exibir dispositivos desabilitados e desconectados.

Para exibir os dispositivos de ponto de extremidade que estão no estado do dispositivo \_ \_ desabilitado e \_ Estados do estado do dispositivo não \_ presentes, clique com o botão direito do mouse na janela Mmsys.cpl e selecione a opção **Mostrar dispositivos desabilitados** .

Para exibir os dispositivos de ponto de extremidade que estão no \_ estado DESconectado do estado do dispositivo \_ , clique com o botão direito do mouse na janela Mmsys.cpl e selecione a opção **Mostrar dispositivos desconectados** .

Para exibir somente os dispositivos de ponto de extremidade que estão no \_ estado ativo do estado do dispositivo \_ , desmarque as opções **Mostrar dispositivos desabilitados** e **Mostrar dispositivos desconectados** .

Para habilitar ou desabilitar um dispositivo de ponto de extremidade no Mmsys.cpl, clique em **reprodução** ou **gravação**, dependendo se o dispositivo é um dispositivo de reprodução ou de gravação. Em seguida, selecione o dispositivo e clique em **Propriedades**. Na janela **Propriedades** , ao lado de **uso do dispositivo**, selecione **usar este dispositivo (habilitar)** ou **não usar este dispositivo (desabilitar)**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Principais constantes de áudio](core-audio-constants.md)
</dt> <dt>

[**IMMDevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**Interface IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




