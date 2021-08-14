---
description: As \_ constantes de sinalizador de bit LINEBEARERMODE descrevem diferentes modos de portador de uma chamada.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Constantes de LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bb03664b6e904cbce7e376eb111675430ea86b8e6880211d76d5b364467097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761760"
---
# <a name="linebearermode_-constants"></a>\_Constantes LINEBEARERMODE

As constantes de sinalizador de bit **LINEBEARERMODE \_** descrevem diferentes modos de portador de uma chamada. Quando um aplicativo faz uma chamada, ele pode solicitar um modo de portador específico. Esses modos são usados para selecionar uma determinada qualidade de serviço para a conexão solicitada da rede de telefone subjacente. Os modos de portador disponíveis em uma determinada linha são uma funcionalidade de dispositivo da linha.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



A transferência alternativa de dados de fala ou irrestrito na mesma chamada (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**dados do LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



A transferência de dados irrestrita na chamada. A taxa de dados é especificada separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ MULTIUSE**
</dt> <dd> <dl> <dt>



O modo Multiuse definido pela ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Isso corresponde a uma conexão de sinalização não associada à chamada do aplicativo ao provedor de serviços ou comutador (Tratado como um fluxo de mídia pela TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**passagem de LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



Quando uma chamada está ativa no LINEBEARERMODE \_ PassThrough, o provedor de serviços fornece acesso direto ao hardware anexado para controle pelo aplicativo. Esse modo é usado principalmente por aplicativos que desejam o controle direto temporário sobre modems assíncronos, acessados por meio das [funções de comunicação](/windows/desktop/DevIO/communications-functions), com a finalidade de configurar ou usar recursos especiais que de outra forma não têm suporte do provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Serviço de portador para dados digitais em que somente os sete bits de ordem inferior de cada octeto podem conter dados do usuário (por exemplo, para o serviço 56Kbit/s comutado).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ fala**
</dt> <dd> <dl> <dt>



Isso corresponde à transmissão de fala G. 711 na chamada. A rede pode usar técnicas de processamento como transmissão analógica, cancelamento de eco e compactação/descompactação. A integridade do bit não é garantida. A fala não tem o objetivo de oferecer suporte a tipos de mídia de fax e modem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ Voice**
</dt> <dd> <dl> <dt>



Este é um serviço de portador de taxa de voz analógica de 3,1 kHz regular. A integridade do bit não é garantida. A voz pode dar suporte a tipos de mídia de fax e modem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

Observe que o modo de portador e o tipo de mídia são noções diferentes. O modo de portador de uma chamada é uma indicação da qualidade da conexão telefônica, conforme fornecido principalmente pela rede. O tipo de mídia de uma chamada é uma indicação do tipo de fluxo de informações que é trocado nessa chamada. O fax do grupo 3 ou o modem de dados são tipos de mídia que usam uma chamada com um modo de portador de voz de 3,1 kHz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

