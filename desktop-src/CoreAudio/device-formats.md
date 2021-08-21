---
description: Formatos de dispositivo
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Formatos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332f3ecd4b30213328552077bdef040a63e31992deaf217b77838dd0cd0797f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957335"
---
# <a name="device-formats"></a>Formatos de dispositivo

para um aplicativo de áudio, um benefício de usar uma API de áudio de nível superior, como DirectSound ou as funções Windows multimídia **waveOutXxx** , é que a API converte automaticamente entre os formatos de fluxo usados pelo aplicativo e os formatos usados pelo dispositivo de áudio. Por outro lado, as principais APIs de áudio são mais restritivas porque exigem que os fluxos de aplicativos usem formatos que são iguais aos ou que estão fortemente relacionados aos formatos usados pelo dispositivo. Assim, os aplicativos que usam as APIs de áudio principal para reproduzir ou gravar fluxos de áudio podem ser necessários para fazer algumas ou todas as conversões entre os formatos de fluxo.

Um aplicativo que usa WASAPI para gerenciar fluxos de modo compartilhado pode contar com o mecanismo de áudio para executar apenas conversões de formato limitadas. O mecanismo de áudio pode converter entre um tamanho de amostra PCM padrão usado pelo aplicativo e os exemplos de ponto flutuante que o mecanismo usa para seu processamento interno. No entanto, o formato de um fluxo de aplicativo normalmente deve ter o mesmo número de canais e a mesma taxa de amostragem que o formato de fluxo usado pelo dispositivo.

Se um aplicativo estiver usando um dispositivo em modo exclusivo, o aplicativo deverá usar um formato de fluxo com suporte explícito para o hardware de áudio. No modo exclusivo, o aplicativo e o dispositivo trocam dados de áudio diretamente, sem intervenção pelo mecanismo de áudio.

Muitos dispositivos de áudio dão suporte a formatos de fluxo PCM e não PCM. No entanto, o mecanismo de áudio pode misturar somente fluxos PCM. Assim, somente os fluxos de modo exclusivo podem ter formatos não PCM. Além disso, somente os formatos não PCM com taxas de dados fixas têm suporte em modo exclusivo. um exemplo de um formato não PCM de taxa fixa é um fluxo de áudio 48-kHz Windows Media audio Professional (WMA Pro) que passa por um link de S/PDIF (interface digital) Sony/Philips no formato digital sem ser decodificado. para obter mais informações sobre como usar o WMA Pro streams sobre S/PDIF, consulte a seguinte documentação:

-   a descrição da marca wave \_ \_ wave WMA \_ -format na documentação do Windows DDK.
-   a white paper intitulada "suporte de Driver de áudio para o formato WMA Pro-over-S/PDIF" no site de [tecnologias do dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

WASAPI usa uma estrutura **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** para especificar um formato de fluxo. Uma estrutura **WAVEFORMATEXTENSIBLE** é efetivamente uma estrutura **WAVEFORMATEX** que foi estendida para descrever uma maior variedade de formatos. Qualquer formato que possa ser descrito por uma estrutura **WAVEFORMATEX** autônoma também pode ser descrito por uma estrutura **WAVEFORMATEXTENSIBLE** .

O primeiro membro da estrutura **WAVEFORMATEXTENSIBLE** é uma estrutura **WAVEFORMATEX** . O conteúdo de uma estrutura **WAVEFORMATEX** indica se é uma estrutura **WAVEFORMATEX** autônoma ou parte de uma estrutura **WAVEFORMATEXTENSIBLE** .

Uma estrutura **WAVEFORMATEX** autônoma pode descrever adequadamente um formato com um ou dois canais e um tamanho de amostra que seja múltiplo de 8 bits. Por si só, uma estrutura **WAVEFORMATEX** não pode especificar o mapeamento de canais para as posições do orador. Além disso, embora **WAVEFORMATEX** especifique o tamanho do contêiner para cada amostra de áudio, ele não pode especificar o número de bits de precisão em uma amostra (por exemplo, 20 bits de precisão em um contêiner de 24 bits). Por outro lado, a estrutura **WAVEFORMATEXTENSIBLE** pode especificar o mapeamento de canais para alto-falantes e o número de bits de precisão em cada amostra.

para obter mais informações sobre **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE**, consulte a documentação do Windows DDK.

a partir do Windows 7, o **WAVEFORMATEXTENSIBLE** foi estendido para representar formatos de dispositivo para transmissão de áudio codificado em uma interface compatível com IEC 61937. Para obter informações sobre a nova estrutura, consulte [representando formatos de transmissões IEC 61937](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Especificando o formato do dispositivo

Os métodos WASAPI a seguir usam as estruturas **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** para descrever os formatos de fluxo:

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

O método **GetMixFormat** recupera o formato de fluxo que o mecanismo de áudio usa para seu processamento interno de fluxos de modo compartilhado. O método sempre usa uma estrutura **WAVEFORMATEXTENSIBLE** , em vez de uma estrutura **WAVEFORMATEX** autônoma, para especificar o formato.

O método **IsFormatSupported** indica se um dispositivo de ponto de extremidade de áudio dá suporte a um formato de fluxo específico. O chamador deve especificar se o formato de fluxo destina-se ao uso em modo compartilhado ou em modo exclusivo. Para formatos de modo compartilhado, o método consulta o mecanismo de áudio para determinar se ele oferece suporte ao formato especificado. Para formatos de modo exclusivo, o método consulta o driver de dispositivo. Alguns drivers de dispositivo relatarão que eles dão suporte a um formato PCM de 1 canal ou 2 canais se o formato for especificado por uma estrutura **WAVEFORMATEX** autônoma, mas rejeitará o mesmo formato se ele for especificado por uma estrutura **WAVEFORMATEXTENSIBLE** . Para obter resultados confiáveis desses drivers, os aplicativos de modo exclusivo devem chamar **IsFormatSupported** duas vezes para cada formato PCM de 1 canal ou 2 canais — uma chamada deve usar uma estrutura **WAVEFORMATEX** autônoma para especificar o formato e a outra chamada deve usar uma estrutura **WAVEFORMATEXTENSIBLE** para especificar o mesmo formato.

Depois que um aplicativo tiver usado **GetMixFormat** ou **IsFormatSupported** para localizar um formato apropriado para um fluxo de modo compartilhado ou de forma exclusiva, o aplicativo poderá chamar o método **Initialize** para inicializar um fluxo com esse formato. Um aplicativo que tenta inicializar um fluxo de modo compartilhado com um formato que não é idêntico ao formato de combinação obtido do método **GetMixFormat** , mas que tem o mesmo número de canais e a mesma taxa de amostragem que o formato Mix, provavelmente terá sucesso. Antes de chamar **Initialize**, o aplicativo pode chamar **IsFormatSupported** para verificar se a **inicialização** aceitará o formato.

O formato de combinação que o mecanismo de áudio usa para seu processamento interno de fluxos de modo compartilhado está fortemente relacionado ao, mas não é necessariamente idêntico ao formato de fluxo que o dispositivo de ponto de extremidade de áudio usa no modo compartilhado. por meio do painel de controle de multimídia Windows, Mmsys.cpl, o usuário pode selecionar o formato de fluxo que um dispositivo de ponto de extremidade de áudio usará quando ele operar no modo compartilhado. As etapas são as seguintes:

1.  Para executar Mmsys.cpl, abra uma janela de prompt de comando e digite o seguinte comando:

    **mmsys.cplde controle**

    Como alternativa, você pode executar Mmsys.cpl clicando com o botão direito do mouse no ícone de alto-falante na área de notificação, que está localizada no lado direito da barra de tarefas e selecionando **dispositivos de reprodução** ou **dispositivos de gravação**.

2.  Depois que a janela de Mmsys.cpl for aberta, selecione um dispositivo na lista de dispositivos de reprodução ou na lista de dispositivos de gravação e clique em **Propriedades**.
3.  Quando a janela Propriedades for aberta, clique em **avançado** e selecione um formato na lista de formatos disponíveis na caixa denominada **formato padrão**.

Por exemplo, suponha que o usuário selecione o seguinte formato padrão na lista de formatos disponíveis para um dispositivo de reprodução:

**2 canais, 16 bits, 44100 Hz (qualidade do CD)**

Esse é o formato que o dispositivo usará subseqüentemente ao operar no modo compartilhado. no Windows Vista, o mecanismo de áudio usará uma versão ligeiramente modificada desse formato para seu processamento interno de fluxos de modo compartilhado. O mecanismo de áudio usará um formato com o mesmo número de canais (dois) e a mesma taxa de amostragem (44100 Hz), mas converterá amostras em números de ponto flutuante antes de processá-los. O mecanismo de áudio converterá os exemplos de ponto flutuante na mistura de saída para inteiros de 16 bits antes de reproduzi-los por meio do dispositivo.

Um aplicativo pode consultar uma propriedade [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) do dispositivo de ponto de extremidade de áudio para obter o formato de modo compartilhado que o usuário selecionou para o dispositivo. Para obter informações sobre como consultar as propriedades de um dispositivo, consulte [Propriedades do dispositivo](device-properties.md).

Alguns aplicativos podem encontrar o formato especificado pela propriedade **PKEY \_ AudioEngine \_ DeviceFormat** de um dispositivo para ser um formato adequado para abrir um fluxo de modo exclusivo no dispositivo. Outros aplicativos que gerenciam fluxos de modo exclusivo podem ter requisitos adicionais que exigem uma negociação de formato complexo com o dispositivo. Normalmente, um desses aplicativos constrói uma lista de formatos adequados, com os formatos preferenciais no início da lista. O aplicativo, em seguida, chama iterativamente o **IsFormatSupported** com cada formato sucessivo na lista, começando no início da lista, até encontrar um formato compatível com o dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 



