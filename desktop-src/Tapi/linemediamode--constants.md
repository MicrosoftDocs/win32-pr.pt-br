---
description: As constantes LINEMEDIAMODE \_ descrevem tipos de mídia (ou modos) de uma sessão ou chamada de comunicação.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: LINEMEDIAMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c11e40a81fffc967afd534ce6de591b524d835cbe97a919903bd97b1eeb4daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140009"
---
# <a name="linemediamode_-constants"></a>Constantes LINEMEDIAMODE \_

As **constantes \_ LINEMEDIAMODE** descrevem tipos de mídia (ou modos) de uma sessão ou chamada de comunicação.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



A energia de voz foi detectada na chamada e a voz é manipulada localmente por um aplicativo automatizado, como com um aplicativo de computador de resposta. Quando um provedor de serviços não consegue distinguir entre a voz interativa e a automatizada em uma chamada de entrada, ele relatará a chamada como voz interativa.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**
</dt> <dd> <dl> <dt>



Uma sessão de modem de dados na chamada. Os protocolos de modem atuais exigem a estação chamada para iniciar o handshake. Para uma chamada de modem de dados de entrada, o aplicativo normalmente não pode fazer nenhuma detecção positiva. Como o provedor de serviços faz essa determinação é sua escolha. Por exemplo, um período de silêncio logo após responder a uma chamada de entrada pode ser usado como heurística para decidir que essa pode ser uma chamada de modem de dados.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Uma sessão ADSI (Interface de Serviços de Exibição Análoga) na chamada. A ADSI aprimora as chamadas de voz com informações alfanuméricos baixadas para o telefone e o uso de botões suaves no telefone.


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



A energia de voz foi detectada na chamada e a chamada é tratada como uma chamada de voz interativa com humanos em ambas as extremidades.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ MIXED**
</dt> <dd> <dl> <dt>



Uma sessão mista na chamada. Misto é um dos serviços telemáticos isdn.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Uma sessão de TDD (Dispositivos de Telefonia para Deficiências) na chamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**
</dt> <dd> <dl> <dt>



Uma sessão de teletex na chamada. Teletex é um dos serviços telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE \_ TELEX**
</dt> <dd> <dl> <dt>



Uma sessão telex na chamada. Telex é um dos serviços telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**VÍDEO DE \_ LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



O tipo de mídia da chamada é vídeo. (TAPI versões 2.1 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Uma sessão de vértice na chamada. O Videotex é um dos serviços telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



O tipo de mídia da chamada é VoiceView. (TAPI versões 1.4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Existe um fluxo de mídia, mas seu modo não é conhecido no momento e pode se tornar conhecido posteriormente. Isso corresponderia a uma chamada com um tipo de mídia não classificado. Em ambientes de telefonia análoga típicos, o tipo de mídia de uma chamada de entrada pode ser desconhecido até que a chamada seja respondida e o fluxo de mídia tenha sido filtrado para fazer uma determinação.

Se o sinalizador de modo de mídia desconhecido estiver definido, outros sinalizadores de mídia também poderão ser definidos. Isso é usado para significar que a mídia é desconhecida, mas que provavelmente é um dos outros tipos de mídia selecionados.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Todos os 32 bits são reservados.

Observe que o modo de portador e o tipo de mídia são noções diferentes. O modo de portador de uma chamada é uma indicação da qualidade da conexão telefônica, conforme fornecido principalmente pela rede. O tipo de mídia de uma chamada é uma indicação do tipo de fluxo de informações que é trocado por essa chamada. O fax do grupo 3 ou modem de dados são tipos de mídia que usam uma chamada com um modo de portador de voz de 3,1 kHz.

Para compatibilidade com versões reversas, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esse valor LINEMEDIAMODE se não tiver suporte na versão \_ negociada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




