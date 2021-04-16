---
description: As constantes de \_ sinalizador de bit PHONESTATE descrevem vários itens de status para um dispositivo de telefone.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Constantes de PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757613"
---
# <a name="phonestate_-constants"></a>Constantes PHONEstate \_

As constantes de sinalizador de bit **PHONESTATE \_** descrevem vários itens de status para um dispositivo de telefone.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**CAPSCHANGE PHONEstate \_**
</dt> <dd> <dl> <dt>



Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) foram alterados. O aplicativo deve usar [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) para ler a estrutura atualizada. Se um provedor de serviços enviar uma mensagem de [**\_ estado de telefone**](phone-state.md) que contém esse valor para a TAPI, a TAPI passará para os aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior receberão mensagens de estado de telefone que \_ especificam a REinicialização de telefone \_


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**TELEFONE \_ conectado**
</dt> <dd> <dl> <dt>



A conexão entre o dispositivo de telefone e a TAPI acabou de ser feita. Isso acontece quando a TAPI é invocada pela primeira vez ou quando a conexão conectada ao telefone com o PC é conectada com a TAPI ativa.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**DEVSPECIFIC PHONEstate \_**
</dt> <dd> <dl> <dt>



As informações específicas do dispositivo do telefone foram alteradas.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**TELEFONEstate \_ desconectado**
</dt> <dd> <dl> <dt>



A conexão entre o dispositivo de telefone e a TAPI acabou de ser quebrada. Isso acontece quando a conexão conectada ao conjunto de telefone para o PC é desconectada enquanto a TAPI está ativa.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**exibição de PHONEstate \_**
</dt> <dd> <dl> <dt>



A exibição do telefone foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**HANDSETGAIN PHONEstate \_**
</dt> <dd> <dl> <dt>



A configuração de lucro do microfone do monofone foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**HANDSETHOOKSWITCH PHONEstate \_**
</dt> <dd> <dl> <dt>



O estado do telefone Hookswitch foi alterado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**HANDSETVOLUME PHONEstate \_**
</dt> <dd> <dl> <dt>



A configuração do volume do palestrante do monofone foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**HEADSETHOOKSWITCH PHONEstate \_**
</dt> <dd> <dl> <dt>



O estado Hookswitch do headset foi alterado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**HEADSETGAIN PHONEstate \_**
</dt> <dd> <dl> <dt>



A configuração de lucro do microfone do headset foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**HEADSETVOLUME PHONEstate \_**
</dt> <dd> <dl> <dt>



A configuração de volume do palestrante do headset foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**lâmpada de PHONEstate \_**
</dt> <dd> <dl> <dt>



Uma lâmpada do telefone foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**monitores de PHONEstate \_**
</dt> <dd> <dl> <dt>



O número de monitores para o dispositivo de telefone.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**outro PHONEstate \_**
</dt> <dd> <dl> <dt>



Itens de status de telefone diferentes daqueles listados abaixo foram alterados. O aplicativo deve verificar o status do telefone atual para determinar quais itens foram alterados.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**proprietário do PHONEstate \_**
</dt> <dd> <dl> <dt>



O número de proprietários para o dispositivo de telefone.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**reinicialização de PHONEstate \_**
</dt> <dd> <dl> <dt>



Os itens foram alterados na configuração de dispositivos de telefone. Para ficar atento a essas alterações (como na aparência de novos dispositivos de telefone), o aplicativo deve reinicializar seu uso da TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONEstate \_ removido**
</dt> <dd> <dl> <dt>



Indica que o dispositivo está sendo removido do sistema pelo provedor de serviços (muito provavelmente por meio de ação do usuário, por meio de um painel de controle ou utilitário semelhante). Uma mensagem de [**\_ estado de telefone**](phone-state.md) com esse valor normalmente será imediatamente seguida por uma mensagem de [**\_ fechamento de telefone**](phone-close.md) no dispositivo. As tentativas subsequentes de acessar o dispositivo antes da TAPI ser reinicializada resultarão no retorno de PHONEERR \_ nodevice para o aplicativo. Se um provedor de serviços enviar uma \_ mensagem de estado de telefone que contenha esse valor para TAPI, a TAPI passará para os aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**retomada de PHONEstate \_**
</dt> <dd> <dl> <dt>



O uso do aplicativo do dispositivo telefônico é retomado após ter sido suspenso por algum tempo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**anéis de TELEFONEstate \_**
</dt> <dd> <dl> <dt>



O modo de anel do telefone foi alterado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**RINGVOLUME PHONEstate \_**
</dt> <dd> <dl> <dt>



O volume de anéis do telefone foi alterado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**SPEAKERHOOKSWITCH PHONEstate \_**
</dt> <dd> <dl> <dt>



O estado Hookswitch do viva-voz foi alterado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**SPEAKERGAIN PHONEstate \_**
</dt> <dd> <dl> <dt>



O estado de configuração de lucro do microfone do viva-voz foi alterado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**SPEAKERVOLUME PHONEstate \_**
</dt> <dd> <dl> <dt>



A configuração de volume do alto-falante do viva-voz foi alterada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**suspensão de PHONEstate \_**
</dt> <dd> <dl> <dt>



O uso do aplicativo do telefone é temporariamente suspenso.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_fechar telefone**](phone-close.md)
</dt> <dt>

[**Estado do telefone \_**](phone-state.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




