---
title: comando Set
description: O comando Set estabelece configurações de controle para o dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- comando set Windows multimídia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc9263ace043f938c8d793b2ceef5ad70264bb1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479482"
---
# <a name="set-command"></a>comando Set

> [!NOTE]
> Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.  Neste documento, há referências à palavra ' escravo '. O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos. Para fins de consistência, este documento contém esta palavra. Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.


O comando Set estabelece configurações de controle para o dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

Sinalizador para estabelecer as configurações de controle. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **set** e os sinalizadores usados por cada tipo.




| Tipo de dispositivo | Sinalizadores de comando | 
|-------------|---------------|
| cdaudio | <ul><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li>porta fechada</li><li>porta aberta</li><li>milissegundos de formato de hora</li><li>meio do formato de hora MSF</li><li>tmsf de formato de hora</li></ul> | 
| digitalvideo | <ul><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li>porta fechada</li><li>porta aberta</li><li><em>formato</em> de formato de arquivo</li><li>buscar exatamente em</li><li>busca exata</li><li><em>fator</em> de velocidade</li><li><em>formato</em> de formato de arquivo ainda</li><li>quadros de formato de hora</li><li>milissegundos de formato de hora</li><li>vídeo desativado</li><li>vídeo ativado</li></ul> | 
| overlay | <ul><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li>porta fechada</li><li>porta aberta</li><li>vídeo desativado</li><li>vídeo ativado</li></ul> | 
| sequenciador | <ul><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li>porta fechada</li><li>porta aberta</li><li>MIDI mestre</li><li>Mestre nenhum</li><li>Mestre SMPTE</li><li><em>tempo</em> de deslocamento</li><li>mapeador de porta</li><li>porta nenhum</li><li><em>port_number</em> de porta</li><li>arquivo subordinado</li><li>MIDI escravo</li><li>nenhum subordinado</li><li>SMPTE-escravo</li><li>tempo <em>tempo_value</em></li><li>milissegundos de formato de hora</li><li>formato de hora SMPTE <em>FPS</em></li><li>drop de formato de hora SMPTE 30</li><li>ponteiro de música de formato de hora</li></ul> | 
| <strong>videocassete</strong> | <ul><li>montar registro em</li><li>montar registro</li><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li><em>hora</em> do relógio</li><li>formato do contador</li><li><em>valor</em> do contador</li><li>porta fechada</li><li>porta aberta</li><li>contador de índice</li><li>data do índice</li><li>hora do índice</li><li>hora do índice</li><li><em>duração</em> de CodeLength</li><li><em>tempo limite</em> de pausa</li><li>duração do registro-</li><li><em>duration</em></li><li>ligar</li><li>desligar</li><li><em>duração</em> da duração da preversão</li><li>formato de registro SP</li><li>formato de registro LP</li><li>formato de registro EP</li><li><em>fator</em> de velocidade</li><li>quadros de formato de hora</li><li>HMS de formato de hora</li><li>milissegundos de formato de hora</li><li>meio do formato de hora MSF</li><li>formato de hora SMPTE <em>FPS</em></li><li>drop de formato de hora SMPTE 30</li><li>tmsf de formato de hora</li><li>contador de modo de tempo</li><li>detecção de modo de tempo</li><li>tempo de vida de modo de hora</li><li>acompanhamento de mais</li><li>menos controle</li><li>redefinição de rastreamento</li></ul> | 
| videodisc | <ul><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li>porta fechada</li><li>porta aberta</li><li>quadros de formato de hora</li><li>HMS de formato de hora</li><li>milissegundos de formato de hora</li><li>faixa de formato de hora</li><li>vídeo desativado</li><li>vídeo ativado</li></ul> | 
| waveaudio | <ul><li><em>inteiro</em> de alinhamento</li><li>qualquer entrada</li><li>qualquer saída</li><li>áudio desativado</li><li>áudio tudo ativado</li><li>áudio restante</li><li>áudio restante em</li><li>áudio à direita</li><li>áudio à direita</li><li><em>bit_count</em> BitsPerSample</li><li><em>byte_rate</em> bytespersec</li><li>canais <em>channel_count</em></li><li>porta fechada</li><li>porta aberta</li><li>formato PCM de marca</li><li>Formatar <em>marca</em> de marca</li><li><em>número inteiro</em> de entrada</li><li><em>número inteiro</em> de saída</li><li>samplespersec <em>inteiro</em></li><li>bytes de formato de hora</li><li>milissegundos de formato de hora</li><li>exemplos de formato de hora</li></ul> | 




 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszSetting** e seus significados.




| Valor | Significado | 
|-------|---------|
| <em>inteiro</em> de alinhamento | Define o alinhamento dos blocos de dados em relação ao início dos dados passados para o dispositivo de forma de onda-áudio. O arquivo é salvo neste formato. | 
| qualquer entrada | Use qualquer entrada que dê suporte ao formato atual durante a gravação. Essa é a configuração padrão. | 
| qualquer saída | Use qualquer saída que dê suporte ao formato atual durante a execução. Esse é o padrão. | 
| montar registro em <br /> montar registro <br /> | No modo de montagem, todas as faixas são registradas conforme definido pelo dispositivo. A maioria dos VCRs estão no modo de montagem por padrão. | 
| áudio desativado <br /> áudio tudo ativado <br /> | Desabilita ou habilita a saída de áudio. Dispositivos de sobreposição de vídeo, o sequenciador MCISEQ e o dispositivo MCIWAVE de onda-áudio não dão suporte a esse sinalizador. | 
| áudio restante <br /> áudio restante em <br /> áudio à direita <br /> áudio à direita <br /> | Desabilita ou habilita a saída para o canal de áudio à esquerda ou à direita. Dispositivos de sobreposição de vídeo, o sequenciador MCISEQ e o dispositivo MCIWAVE de onda-áudio não dão suporte a esse sinalizador. | 
| <em>bit_count</em> BitsPerSample | Define o número de bits por amostra do PCM (modulação de código de pulso) reproduzido ou registrado. O arquivo é salvo neste formato. | 
| <em>byte_rate</em> bytespersec | Define o número médio de bytes por segundo reproduzidos ou registrados. O arquivo é salvo neste formato. | 
| canais <em>channel_count</em> | Define os canais para reprodução e gravação. O arquivo é salvo neste formato. | 
| <em>hora</em> do relógio | Define a hora no relógio externo para a <em>hora.</em> O formato é especificado como um inteiro não assinado longo. | 
| formato do contador | Defina o formato de hora para o contador, conforme retornado pelo <a href="status.md">status</a> "Counter". Para obter informações sobre os tipos aplicáveis, consulte o comando <strong>set</strong> "Time Format". | 
| <em>valor</em> do contador | Define o contador de VCR para o valor especificado. O valor deve ser especificado no formato de contador atual. Para obter mais informações, consulte o comando <strong>set</strong> "Counter Format". | 
| porta fechada | Cancela a bandeja e fecha a porta, se possível. Para VCRs, o carrega a fita automaticamente. | 
| porta aberta | Abre a porta e ejeta a bandeja ou fita, se possível. | 
| <em>formato</em> de formato de arquivo | Especifica um formato de arquivo que é usado para <a href="save.md">salvar</a> ou <a href="capture.md">capturar</a> comandos. Se omitido, isso pode padronizar para um formato definido por driver de dispositivo. Se o formato de arquivo especificado estiver em conflito com o algoritmo e a qualidade selecionados no momento, eles serão alterados para os padrões para o formato de arquivo. Os seguintes formatos de arquivo são definidos:<ul><li>AVI: especifica o formato AVI.</li><li>avss: especifica o formato AVSS.</li><li>DIB: especifica o formato DIB.</li><li>JFIF: especifica o formato JFIF.</li><li>JPEG: especifica o formato JPEG.</li><li>MPEG: especifica o formato MPEG.</li><li>rdib: especifica o formato de DIB RLE.</li><li>rjpeg: especifica o formato RJPEG.</li></ul> | 
| formato PCM de marca | Define o tipo de formato como PCM para reprodução e gravação. O arquivo é salvo neste formato. | 
| Formatar <em>marca</em> de marca | Define o tipo de formato para reprodução e gravação. O arquivo é salvo neste formato. | 
| índice de código de <br /> contador de índice <br /> data do índice <br /> hora do índice <br /> | Define a tela de exibição atual no VCR. | 
| <em>número inteiro</em> de entrada | Define o canal de áudio usado como entrada. | 
| <em>duração</em> do comprimento | Define o comprimento especificado pelo usuário da fita no VCR. Esse comprimento é retornado pelo comando de <a href="status.md">status</a> "Length" e é fornecido para compatibilidade com aplicativos que exigem que esse comando retorne um comprimento válido. | 
| MIDI mestre | Define o sequenciador MIDI como a origem da sincronização. Os dados de sincronização são enviados no formato MIDI. O sequenciador MCISEQ não dá suporte a esse sinalizador. | 
| Mestre nenhum | Inibe o sequenciador MIDI de enviar dados de sincronização. O sequenciador MCISEQ não dá suporte a esse sinalizador. | 
| Mestre SMPTE | Define o sequenciador MIDI como a origem da sincronização. Os dados de sincronização são enviados em formato SMPTE (sociedade de imagem e engenheiros de televisão). O sequenciador MCISEQ não dá suporte a esse sinalizador. | 
| <em>tempo</em> de deslocamento | Define o <em>tempo</em>de deslocamento SMPTE. O deslocamento é a hora de início de uma sequência baseada em SMPTE. O <em>tempo</em> é expresso como <em>hh</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, em que <em>hh</em> é hours, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames. | 
| <em>número inteiro</em> de saída | Define o canal de áudio usado como a saída. | 
| <em>tempo limite</em> de pausa | Define a duração máxima, em milissegundos, de um comando de <a href="pause.md">pausa</a> . Um valor de <em>tempo limite</em> igual a zero indica que nenhum tempo limite ocorrerá. | 
| <em>duração</em> da duração do registro | Define o comprimento, no formato de hora atual, necessário para <a href="stop.md">finalizar</a> o transporte de videocassete quando um comando Stop ou <strong>Pause</strong> é emitido. | 
| mapeador de porta | Define o mapeador de MIDI como a porta que recebe as mensagens de MIDI. Esse comando falhará se o mapeador de MIDI ou uma porta necessária estiver sendo usado por outro aplicativo. | 
| porta nenhum | Desabilita o envio de mensagens MIDI. Esse comando também fecha uma porta MIDI. | 
| <em>port_number</em> de porta | Define a porta MIDI que recebe as mensagens MIDI. Esse comando falhará se a porta que você está tentando abrir estiver sendo usada por outro aplicativo. | 
| ligar <br /> desligar <br /> | Define a energia do dispositivo como on ou off. | 
| <em>duração</em> da duração da preversão | Define o comprimento, no formato de hora atual, necessário para estabilizar a saída de VCR. | 
| formato de registro SP <br /> formato de registro LP <br /> formato de registro EP <br /> | Define o modo de gravação para o VCR para o SP para Play Standard, EP para reprodução estendida ou LP para reprodução longa. Esses valores não se destinam a ser específicos de VHS. Eles são mapeados para quaisquer três modos apropriados com outros formatos de fita. Por exemplo, o SP é mapeado para a gravação mais rápida e de qualidade mais alta. | 
| samplespersec <em>inteiro</em> | Define a taxa de amostra para reprodução e gravação. O arquivo é salvo neste formato. | 
| buscar exatamente em<br /> busca exata <br /> | Seleciona um dos dois modos de busca. Com "Seek exactly on", a busca sempre será movida para o quadro especificado. Com "Seek exactly off", Seek passará para o quadro-chave mais próximo antes do quadro especificado. | 
| arquivo subordinado | Define o sequenciador MIDI para usar dados de arquivo como a origem da sincronização. Essa é a configuração padrão. | 
| slave midi | Define o sequenciador MIDI para usar dados MIDI de entrada para a origem da sincronização. O sequenciador reconhece dados de sincronização com o formato MIDI. O sequenciador MCISEQ não dá suporte a esse sinalizador. | 
| slave none | Define o sequenciador MIDI para ignorar a sincronização | 
| smpte de slave | Define o sequenciador MIDI para usar dados MIDI de entrada para a origem da sincronização. O sequenciador reconhece dados de sincronização com o formato SMPTE. O sequenciador MCISEQ não dá suporte a esse sinalizador. | 
| fator de velocidade | Define a velocidade relativa da reprodução de áudio e vídeo do workspace. Fator é a taxa entre a taxa de quadros nominal e a taxa de quadros desejada, em que a taxa de quadros nominal é designada como 1000. (Uma taxa de 500 é metade da velocidade normal, 2000 é duas vezes a velocidade normal e assim por diante.) Definir a velocidade como zero reproduz o vídeo o mais rápido possível sem soltar quadros e sem áudio. | 
| formato de formato de <em>arquivo ainda</em> | Especifica o formato de arquivo usado para comandos de captura. | 
| tempo tempo_value | Define o tempo da sequência de acordo com o formato de hora atual. Para um arquivo baseado em PPQN, o tempo_value é interpretado como ritmos por minuto. Para um arquivo baseado em SMPTE, o tempo_value é interpretado como quadros por segundo. | 
| bytes de formato de tempo | Em um formato de arquivo PCM, define o formato de hora como bytes. Todas as informações de posição são especificadas como bytes após este comando. | 
| quadros de formato de tempo | Define o formato de hora como quadros. Todos os comandos que usam valores de posição assumirão quadros. Quando o dispositivo é aberto, os quadros são o modo padrão. Com suporte em videodiscs usando o formato PDF. | 
| formato de tempo hms | Define o formato de hora como horas, minutos e segundos. Todos os comandos que usam valores de posição assumirão o HMS. HMS é o formato padrão para videodiscs CLV. Especifique um valor HMS como hh:mm:ss, em que hh é horas, mm é minutos e ss é segundos. Você poderá omitir um campo se ele e todos os campos a seguir são zero. Por exemplo, 3, 3:0 e 3:0:0 são maneiras válidas de expressar 3 horas. <br /> | 
| formato de tempo milissegundos | Define o formato de hora como milissegundos. Todos os comandos que usam valores de posição assumirão milissegundos. Você pode abreviar milissegundos como "ms". Para dispositivos sequenciais, o arquivo de sequência define o formato padrão como PPQN ou SMPTE. Os dispositivos de sobreposição de vídeo não são compatíveis com esse sinalizador.<br /> | 
| time format msf | Define o formato de hora como minutos, segundos e quadros. Todos os comandos que usam valores de posição assumirão o MSF (o formato padrão para áudio de CD). Especifique um valor MSF como mm:ss:ff, em que mm é minutos, ss é segundos e ff é quadros. Você poderá omitir um campo se ele e todos os campos a seguir são zero. Por exemplo, 3, 3:0 e 3:0:0 são maneiras válidas de expressar 3 minutos.<br /> Os campos do MSF têm os seguintes valores máximos:<br /><ul><li>Minutos 99</li><li>Segundos 59</li><li>Quadros 74</li></ul> | 
| exemplos de formato de tempo | Define o formato de hora como exemplos. Todas as informações de posição são especificadas como exemplos após este comando. | 
| time format smpte 24<br /> time format smpte 25<br /> time format smpte 30<br /> | Define o formato de hora como uma taxa de quadros SMPTE. Para VCRs, define o formato de hora como hh:mm:ss:ff, em que os valores legais são 00:00:00:00 a 23:59:59:xx e xx é um a menos que os quadros por segundo, conforme especificado pelo número 24, 25 ou 30, conforme especificado no sinalizador. Na entrada, dois-pontos (:) são necessários para separar os componentes. As unidades menos significativas poderão ser omitidas se elas são 00; por exemplo, 02:00 é o mesmo que 02:00:00:00. Todos os comandos que usam valores de posição assumirão o formato SMPTE.<br /> O arquivo de sequência define o formato padrão como PPQN ou SMPTE.<br /> | 
| time format smpte 30 drop | Define o formato de hora como taxa de quadros de redução de SMPTE 30. Para VCRs, o mesmo que o SMPTE 30, exceto que determinadas posições de código de data/hora são retiradas do formato para que as posições de código de hora registradas para cada quadro (na taxa de quadros NTSC de 29,97 fps) correspondam ao tempo real (a 30 fps). As posições de código de tempo que são descartados são as opções a seguir: duas a cada minuto, no minuto, para os primeiros nove de cada dez minutos de conteúdo gravado. Por exemplo, às 01:04:59:29, a próxima posição do código de hora seria 01:05:00:02, não 01:05:00:00. Todos os comandos que usam valores de posição assumirão o formato SMPTE.<br /> O arquivo de sequência define o formato padrão como PPQN ou SMPTE.<br /> | 
| ponteiro de música de formato de hora | Define o formato de hora como ponteiro de música (décimo sexto anotações). Todos os comandos que usam valores de posição assumirão unidades de ponteiro de música. Esse sinalizador é válido apenas para uma sequência do tipo de divisão PPQN. | 
| time format tmsf | Define o formato de hora como faixas, minutos, segundos e quadros. Todos os comandos que usam valores de posição assumirão o TMSF. Especifique um valor TMSF como tt:mm:ss:ff, em que tt é faixas, mm é minutos, ss é segundos e ff é quadros. Você poderá omitir um campo se ele e todos os campos a seguir são zero. Por exemplo, 3, 3:0, 3:0:0 e 3:0:0:0 são todas maneiras válidas de expressar a faixa 3. <br /> Os campos TMSF têm os seguintes valores máximos:<br /><ul><li>Faixas 99</li><li>Minutos 90</li><li>Segundos 59</li><li>Quadros 74</li></ul> | 
| faixa de formato de tempo | Define o formato de posição como faixas. Todos os comandos que usam valores de posição assumirão faixas. | 
| contador de modo de tempo | Define o modo de posição-informação para usar os contadores de VCR. | 
| detecção de modo de tempo | Define o modo de informações de posição com base na detecção de informações de código de data/hora na fita. Se as informações de código de data/hora são detectadas, o tipo de hora é definido como "timecode"; caso contrário, o tipo de hora será definido como "contador". "Detectar" é um modo especial. Sempre que o driver é aberto, uma nova fita é inserida ou o comando "modo de tempo" é emitido, o driver verifica o modo de hora atual disponível na fita e define "tipo de tempo" como "timecode" ou "counter". Depois que o "tipo de hora" for definido, o driver não o alterará até que uma das condições acima ocorra novamente.<br /> | 
| time mode timecode | Define o modo de informações de posição para usar informações de "código de tempo" na fita. | 
| acompanhamento de mais <br /> acompanhamento de menos <br /> redefinição de acompanhamento <br /> | Ajusta a velocidade do transporte de fitas em incrementos finos. Use os sinalizadores de "acompanhamento" quando uma imagem com voz for obtida de um VCR. "Acompanhamento de mais" aumenta a velocidade do transporte. "Acompanhamento de menos" diminui a velocidade de transporte. "Redefinição de acompanhamento" retorna o ajuste de acompanhamento para zero. | 
| vídeo desligado | Desabilita a saída de vídeo. | 
| vídeo em | Habilita a saída de vídeo. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Várias propriedades de dados waveform-audio são definidas quando o arquivo para armazenar os dados é criado. Essas propriedades descrevem como os dados são estruturados dentro do arquivo e não podem ser alterados depois que a gravação é iniciada. A lista a seguir identifica estas propriedades:

-   alinhamento
-   bitspersample
-   bytespersec
-   canais
-   format tag
-   samplespersec

## <a name="examples"></a>Exemplos

O comando a seguir define o formato de tempo como milissegundos e define o formato waveform-audio como 8 bits, mono, 11 kHz.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[Capturar](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[salvar](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

