---
description: As \_ constantes LINEMEDIAMODE descrevem os tipos de mídia (ou modos) de uma sessão ou chamada de comunicação.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Constantes de LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758401"
---
# <a name="linemediamode_-constants"></a>\_Constantes LINEMEDIAMODE

As **constantes \_ LINEMEDIAMODE** descrevem os tipos de mídia (ou modos) de uma sessão ou chamada de comunicação.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



A energia de voz foi detectada na chamada, e a voz é manipulada localmente por um aplicativo automatizado, como com um aplicativo de secretária automática. Quando um provedor de serviços não pode distinguir entre voz interativa e automatizada em uma chamada de entrada, ele relatará a chamada como voz interativa.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAmode**
</dt> <dd> <dl> <dt>



Uma sessão de modem de dados na chamada. Os protocolos de modem atuais exigem que a estação chamada inicie o handshake. Para uma chamada de modem de dados de entrada, o aplicativo normalmente pode não fazer nenhuma detecção positiva. Como o provedor de serviços faz essa determinação é sua escolha. Por exemplo, um período de silêncio logo após responder a uma chamada de entrada pode ser usado como uma heurística para decidir que isso pode ser uma chamada de modem de dados.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Uma sessão ADSI (interface de serviços de vídeo analógico) na chamada. A ADSI aprimora chamadas de voz com informações alfanuméricas baixadas para o telefone e o uso de botões suaves no telefone.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



Um fluxo de dados digital de formato não especificado.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



Um fax do grupo 3 está sendo enviado ou recebido pela chamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



Um fax do grupo 4 está sendo enviado ou recebido pela chamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



A energia de voz foi detectada na chamada, e a chamada é tratada como uma chamada de voz interativa com seres humanos em ambas as extremidades.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ misto**
</dt> <dd> <dl> <dt>



Uma sessão mista na chamada. Misto é um dos serviços ISDN telemática.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**\_TDD LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Uma sessão TDD (dispositivos de telefonia para a surdo) na chamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ Teletex**
</dt> <dd> <dl> <dt>



Uma sessão Teletex na chamada. Teletex é um dos serviços telemáticas.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**TELEX do LINEMEDIAMODE \_**
</dt> <dd> <dl> <dt>



Uma sessão de telex na chamada. O telex é um dos serviços telemáticas.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**vídeo do LINEMEDIAMODE \_**
</dt> <dd> <dl> <dt>



O tipo de mídia da chamada é vídeo. (TAPI versões 2,1 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Uma sessão videotex na chamada. Videotex é um dos serviços telemáticas.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



O tipo de mídia da chamada é VoiceView. (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ desconhecido**
</dt> <dd> <dl> <dt>



Um fluxo de mídia existe, mas seu modo não é conhecido no momento e pode ser conhecido mais tarde. Isso corresponderia a uma chamada com um tipo de mídia não classificado. Em ambientes de telefonia analógicos típicos, o tipo de mídia de uma chamada de entrada pode ser desconhecido até que a chamada tenha sido respondida e o fluxo de mídia tenha sido filtrado para fazer uma determinação.

Se o sinalizador de modo de mídia desconhecido for definido, outros sinalizadores de mídia também poderão ser definidos. Isso é usado para significar que a mídia é desconhecida, mas é provável que seja um dos outros tipos de mídia selecionados.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Todos os 32 bits são reservados.

Observe que o modo de portador e o tipo de mídia são noções diferentes. O modo de portador de uma chamada é uma indicação da qualidade da conexão telefônica, conforme fornecido principalmente pela rede. O tipo de mídia de uma chamada é uma indicação do tipo de fluxo de informações que é trocado nessa chamada. O fax do grupo 3 ou o modem de dados são tipos de mídia que usam uma chamada com um modo de portador de voz de 3,1 kHz.

Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esse valor de LINEMEDIAMODE \_ se não houver suporte na versão negociada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




