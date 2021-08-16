---
description: As constantes de sinalizador de bits LINEBEARERMODE \_ descrevem diferentes modos de portador de uma chamada.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: LINEBEARERMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bb03664b6e904cbce7e376eb111675430ea86b8e6880211d76d5b364467097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761760"
---
# <a name="linebearermode_-constants"></a>Constantes LINEBEARERMODE \_

As constantes de sinalizador de bits **LINEBEARERMODE \_** descrevem diferentes modos de portador de uma chamada. Quando um aplicativo faz uma chamada, ele pode solicitar um modo de portador específico. Esses modos são usados para selecionar uma determinada qualidade de serviço para a conexão solicitada da rede telefônica subjacente. Os modos de portador disponíveis em uma determinada linha são uma funcionalidade do dispositivo da linha.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



A transferência alternativa de fala ou dados irrestritos na mesma chamada (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**DADOS LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



A transferência de dados irrestrita na chamada. A taxa de dados é especificada separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ MULTIUSE**
</dt> <dd> <dl> <dt>



O modo multiuso definido pelo ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Isso corresponde a uma conexão de sinalização não associada à chamada do aplicativo ao provedor de serviços ou à opção (tratada como um fluxo de mídia pela TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**PASSAGEM LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



Quando uma chamada está ativa em LINEBEARERMODE PASSTHROUGH, o provedor de serviços fornece acesso direto ao \_ hardware anexado para controle pelo aplicativo. Esse modo é usado principalmente por aplicativos que desejam controle direto temporário sobre modems assíncronos, acessados por meio das funções de comunicação [,](/windows/desktop/DevIO/communications-functions)com a finalidade de configurar ou usar recursos especiais sem suporte do provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Serviço de portador para dados digitais em que apenas os sete bits de ordem baixa de cada octeto podem conter dados de usuário (por exemplo, para o serviço Comutado de 56kbits/s).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**FALA LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



Isso corresponde à transmissão de fala G.711 na chamada. A rede pode usar técnicas de processamento, como transmissão análoga, cancelamento de eco e compactação/descompactação. A integridade do bit não é garantida. A fala não se destina a dar suporte a tipos de mídia de fax e modem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ VOICE**
</dt> <dd> <dl> <dt>



Esse é um serviço de portador de nível de voz análogo normal de 3,1 kHz. A integridade do bit não é garantida. A voz pode dar suporte a tipos de mídia de fax e modem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem alta podem ser atribuídos a extensões específicas do dispositivo. Os 16 bits de ordem baixa são reservados.

Observe que o modo de portador e o tipo de mídia são noções diferentes. O modo de portador de uma chamada é uma indicação da qualidade da conexão telefônica, conforme fornecido principalmente pela rede. O tipo de mídia de uma chamada é uma indicação do tipo de fluxo de informações que é trocado por essa chamada. O fax do grupo 3 ou modem de dados são tipos de mídia que usam uma chamada com um modo de portador de voz de 3,1 kHz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

