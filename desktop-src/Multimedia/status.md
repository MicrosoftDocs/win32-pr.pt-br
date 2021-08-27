---
title: comando de status
description: O comando status solicita informações de status de um dispositivo. Todos os dispositivos reconhecem este comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando de status Windows multimídia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd209ed04e51671ce7d9c8a7ae88a79073836c2e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626104"
---
# <a name="status-command"></a>comando de status

> [!NOTE]
> Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.  Neste documento, há referências à palavra ' escravo '. O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos. Para fins de consistência, este documento contém esta palavra. Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.

O comando status solicita informações de status de um dispositivo. Todos os dispositivos reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Sinalizador para solicitar informações de status. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **status** e os sinalizadores usados por cada tipo.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dispositivo</th>
<th>Sinalizadores de solicitação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li><em>número</em> de faixa do tipo cdaudio</li>
<li>faixa atual</li>
<li>comprimento</li>
<li><em>número</em> de faixa de comprimento</li>
<li>mídia presente</li>
<li>mode</li>
<li>número de faixas</li>
<li>position</li>
<li><em>número</em> da faixa de posição</li>
<li>esteja</li>
<li>posição inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>áudio</li>
<li>alinhamento de áudio</li>
<li>BitsPerSample de áudio</li>
<li>quebras de áudio</li>
<li>bytespersec de áudio</li>
<li>entrada de áudio</li>
<li>registro de áudio</li>
<li>fonte de áudio</li>
<li>samplespersec de áudio</li>
<li>fluxo de áudio</li>
<li>graves</li>
<li>bitsperpel</li>
<li>lo</li>
<li>cor</li>
<li>contraste</li>
<li>faixa atual</li>
<li><em>unidade</em> de espaço em disco</li>
<li>conclusão do arquivo</li>
<li>formato de arquivo</li>
<li>modo de arquivo</li>
<li>avançar</li>
<li>quadros ignorados</li>
<li>gamma</li>
<li>input</li>
<li>volume esquerdo</li>
<li>comprimento</li>
<li><em>número</em> de faixa de comprimento</li>
<li>mídia presente</li>
<li>mode</li>
<li>monitor</li>
<li>método de monitor</li>
<li>nominal</li>
<li>taxa de quadros nominal</li>
<li>taxa de quadros de registro nominal</li>
<li>número de faixas</li>
<li>output</li>
<li>identificador da paleta</li>
<li>modo de pausa</li>
<li>velocidade de reprodução</li>
<li>position</li>
<li><em>número</em> da faixa de posição</li>
<li>esteja</li>
<li>taxa de quadros de registro</li>
<li><em>quadro</em> de referência</li>
<li>Tamanho reservado</li>
<li>volume correto</li>
<li>buscar exatamente</li>
<li>nitidez</li>
<li>SMPTE</li>
<li>velocidade</li>
<li>posição inicial</li>
<li>formato de arquivo ainda</li>
<li>formato de hora</li>
<li>Nuance</li>
<li>agudo</li>
<li>não salvas</li>
<li>video</li>
<li>índice de chave de vídeo</li>
<li>cor da chave do vídeo</li>
<li>registro de vídeo</li>
<li>fonte de vídeo</li>
<li>número da fonte do vídeo</li>
<li>fluxo de vídeo</li>
<li>volume</li>
<li>alça de janela</li>
<li>janela visível</li>
<li>janela minimizada</li>
<li>janela maximizada</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>mídia presente</li>
<li>mode</li>
<li>número de faixas</li>
<li>Pronto</li>
<li>Esticar</li>
<li>alça de janela</li>
</ul></td>
</tr>
<tr class="even">
<td>sequenciador</td>
<td><ul>
<li>faixa atual</li>
<li>tipo de divisão</li>
<li>comprimento</li>
<li>length track <em>number</em> master</li>
<li>mídia presente</li>
<li>mode</li>
<li>número de faixas</li>
<li>deslocamento</li>
<li>porta</li>
<li>position</li>
<li>número da faixa de <em>posição</em></li>
<li>Pronto</li>
<li>Escravo</li>
<li>posição inicial</li>
<li>tempo</li>
<li>formato de tempo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Videocassete</td>
<td><ul>
<li>montar registro</li>
<li>monitor de áudio</li>
<li>número do monitor de áudio</li>
<li>registro de áudio</li>
<li>número da faixa de registro de <em>áudio</em></li>
<li>fonte de áudio</li>
<li>número da fonte de áudio</li>
<li>channel</li>
<li>número do tuner de <em>canal</em></li>
<li>clock</li>
<li>ID do relógio</li>
<li>contador</li>
<li>formato do contador</li>
<li>resolução de contador</li>
<li>faixa atual</li>
<li>taxa de quadros</li>
<li>índice</li>
<li>índice em</li>
<li>comprimento</li>
<li>número da faixa de <em>comprimento</em></li>
<li>mídia presente</li>
<li>tipo de mídia</li>
<li>mode</li>
<li>número de faixas de áudio</li>
<li>número de faixas</li>
<li>número de faixas de vídeo</li>
<li>tempo <em>de pausa</em></li>
<li>formato de reprodução</li>
<li>position</li>
<li>position start</li>
<li>número da faixa de <em>posição</em></li>
<li>duração do <em>pós-roll</em></li>
<li>power on</li>
<li>duração do <em>pré-roll</em></li>
<li>Pronto</li>
<li>formato de registro</li>
<li>velocidade</li>
<li>formato de tempo</li>
<li>modo de tempo</li>
<li>tipo de tempo</li>
<li>timecode present</li>
<li>registro de código de hora</li>
<li>tipo de código de hora</li>
<li>número do tuner</li>
<li>monitor de vídeo</li>
<li>número do monitor de vídeo</li>
<li>registro de vídeo</li>
<li>número da faixa de registro de <em>vídeo</em></li>
<li>origem do vídeo</li>
<li>número de origem do vídeo</li>
<li>gravação protegida</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>faixa atual</li>
<li>tamanho do disco</li>
<li>avançar</li>
<li>comprimento</li>
<li>número da faixa de <em>comprimento</em></li>
<li>mídia presente</li>
<li>tipo de mídia</li>
<li>mode</li>
<li>número de faixas</li>
<li>position</li>
<li>número da faixa de <em>posição</em></li>
<li>Pronto</li>
<li>Lado</li>
<li>velocidade</li>
<li>posição inicial</li>
<li>formato de tempo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Waveaudio</td>
<td><ul>
<li>alinhamento</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>canais</li>
<li>faixa atual</li>
<li>format tag</li>
<li>input</li>
<li>comprimento</li>
<li>número da faixa de <em>comprimento</em></li>
<li>nível</li>
<li>mídia presente</li>
<li>mode</li>
<li>número de faixas</li>
<li>output</li>
<li>position</li>
<li>número da faixa de <em>posição</em></li>
<li>Pronto</li>
<li>samplespersec</li>
<li>posição inicial</li>
<li>formato de tempo</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista os sinalizadores que podem ser especificados no **parâmetro lpszRequest** e seus significados.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>alinhamento</td>
<td>Retorna o alinhamento de bloco de dados, em bytes.</td>
</tr>
<tr class="even">
<td>montar registro</td>
<td>Retornará <strong>TRUE</strong> se o dispositivo estiver definido para montar a gravação do modo.</td>
</tr>
<tr class="odd">
<td>áudio</td>
<td>Retorna &quot; &quot; &quot; dependendo &quot; do comando <a href="setaudio.md">setaudio on</a> ou off mais &quot; &quot; &quot; &quot; recente. Ele &quot; retornará se &quot; um ou ambos os alto-falantes estão habilitados e desligados caso &quot; &quot; contrário.</td>
</tr>
<tr class="even">
<td>alinhamento de áudio</td>
<td>Retorna o alinhamento dos blocos de dados em relação ao início dos dados de áudio de forma de onda de entrada.</td>
</tr>
<tr class="odd">
<td>audio bitspersample</td>
<td>Retorna o número de bits por exemplo que o dispositivo usa para gravação. Esse sinalizador se aplica somente a dispositivos que suportam o &quot; algoritmo &quot; pcm.</td>
</tr>
<tr class="even">
<td>quebras de áudio</td>
<td>Retorna o número de vezes que a parte de áudio da última sequência AVI foi quebrada. O sistema conta uma quebra de áudio sempre que tenta gravar dados de áudio no driver do dispositivo e descobre que o driver já tocada todos os dados disponíveis. Esse sinalizador é reconhecido apenas pelo driver de vídeo digital MCIAVI. Ele se trata apenas da avaliação de desempenho; o valor de retorno é difícil de interpretar.</td>
</tr>
<tr class="odd">
<td>bytes de áudiopersec</td>
<td>Retorna o número médio de bytes por segundo usado para gravação.</td>
</tr>
<tr class="even">
<td>entrada de áudio</td>
<td>Retorna o nível de áudio instantâneo aproximado do sinal de áudio de entrada análogo. Um valor maior que 1000 implica distorção de recorte. Alguns dispositivos só podem retornar esse valor durante a gravação de áudio. O valor não tem nenhum comando <a href="set.md">set ou</a> <a href="setaudio.md">setaudio</a> associado.</td>
</tr>
<tr class="odd">
<td>monitor de áudio</td>
<td>Retorna &quot; a saída ou um dos tipos de entrada de &quot; origem válidos. Para obter mais informações, consulte o <strong>comando setaudio</strong> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>número do monitor de áudio</td>
<td>Retorna o número de vídeo monitorado do tipo especificado pelo <strong>monitor de áudio de status</strong> &quot; &quot; . Para obter mais informações, consulte o <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="odd">
<td>registro de áudio</td>
<td>Retorna &quot; on ou off , &quot; &quot; &quot; refletindo o estado definido pelo registro <strong>setaudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>número da faixa de registro de <em>áudio</em></td>
<td>Retornará <strong>TRUE</strong> se o VCR estiver definido para gravar áudio. Se nenhum número de faixa for determinado, o valor padrão de 1 será assumido.</td>
</tr>
<tr class="odd">
<td>audio samplespersec</td>
<td>Retorna o número de amostras por segundo registradas.</td>
</tr>
<tr class="even">
<td>fonte de áudio</td>
<td>Retorna a fonte atual do digitalizador de áudio: &quot; &quot; esquerda, &quot; &quot; direita, &quot; média ou &quot; &quot; estéreo. &quot;</td>
</tr>
<tr class="odd">
<td>número da fonte de áudio</td>
<td>Retorna o número de fonte de áudio do tipo retornado pela fonte de <strong>áudio de status</strong> &quot; &quot; . Para obter mais informações, consulte o <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="even">
<td>fluxo de áudio</td>
<td>Retorna o número atual do fluxo de áudio.</td>
</tr>
<tr class="odd">
<td>Baixo</td>
<td>Retorna o nível de áudio atual.</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>Retorna o número de bits por pixel para salvar dados capturados ou gravados.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Retorna os bits por exemplo.</td>
</tr>
<tr class="even">
<td>Brilho</td>
<td>Retorna o nível atual de brilho de vídeo.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Retorna o número médio de bytes por segundo tocados ou gravados.</td>
</tr>
<tr class="even">
<td>número da faixa <em></em> do tipo cdaudio</td>
<td>Retorna o tipo do número de faixa especificado. Pode ser áudio &quot; &quot; ou &quot; outro.&quot;</td>
</tr>
<tr class="odd">
<td>channel</td>
<td>Retorna o valor inteiro do canal definido no ajuste.</td>
</tr>
<tr class="even">
<td>número do tuner de <em>canal</em></td>
<td>Se o número do ajuste for determinado, o &quot; canal selecionado no momento no número do ajuste &quot; <em></em> <em>lógico</em> será retornado. Observe que pode haver vários ajuste lógicos.</td>
</tr>
<tr class="odd">
<td>canais</td>
<td>Retorna o número de canais definidos (1 para mono, 2 para estéreo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Retorna a hora externa. O tempo deve ser um inteiro longo sem sinal expressando incrementos totais. Para obter mais informações, consulte o <a href="capability.md">comando taxa de</a> incremento do relógio de &quot; &quot; funcionalidade.</td>
</tr>
<tr class="odd">
<td>ID do relógio</td>
<td>Retorna um inteiro exclusivo que identifica o relógio.</td>
</tr>
<tr class="even">
<td>cor</td>
<td>Retorna o nível de cor atual.</td>
</tr>
<tr class="odd">
<td>contraste</td>
<td>Retorna o nível de contraste atual.</td>
</tr>
<tr class="even">
<td>contador</td>
<td>Retorna a posição do contador, no formato de contador atual.</td>
</tr>
<tr class="odd">
<td>formato do contador</td>
<td>Retorna o formato do contador atual. Para obter mais informações, consulte o comando <a href="set.md">set</a> &quot; counter &quot; format.</td>
</tr>
<tr class="even">
<td>resolução de contador</td>
<td>Retorna &quot; quadros ou segundos , &quot; &quot; &quot; indicando a resolução do contador. Isso não é o mesmo que a precisão.</td>
</tr>
<tr class="odd">
<td>faixa atual</td>
<td>Retorna a faixa atual. O sequenciador MCISEQ retorna 1.</td>
</tr>
<tr class="even">
<td>tamanho do disco</td>
<td>Retorna 8 ou 12, indicando o tamanho do disco carregado em polegadas.</td>
</tr>
<tr class="odd">
<td>unidade de espaço em <em>disco</em></td>
<td>Retorna o espaço em disco aproximado, no formato de hora atual, que pode ser obtido por um comando <a href="reserve.md">de</a> reserva para a unidade de disco <em>especificada.</em> A <em>unidade</em> geralmente é especificada como uma única letra ou uma única letra seguida por dois-pontos (:). No entanto, alguns dispositivos podem usar um caminho.</td>
</tr>
<tr class="even">
<td>tipo de divisão</td>
<td>Retorna um dos seguintes tipos de divisão de arquivo:
<ul>
<li>PPQN</li>
<li>Quadro SMPTE 24</li>
<li>Quadro SMPTE 25</li>
<li>Quadro de soltar do SMPTE 30</li>
<li>Quadro SMPTE 30</li>
</ul>
<br/> Use essas informações para determinar o formato do arquivo MIDI e o significado das informações de tempo e posição.<br/></td>
</tr>
<tr class="odd">
<td>conclusão de arquivo</td>
<td>Retorna o percentual estimado em que uma <a href="load.md">operação de</a>carregamento , <a href="save.md">salvar</a> <a href="capture.md">,</a>capturar , <a href="cut.md">recortar</a> <a href="copy.md"></a> <a href="delete.md">,</a>copiar <a href="paste.md">,</a>excluir , colar <a href="undo.md">ou</a> desfazer progride. (Os aplicativos podem usar isso para fornecer um indicador visual de progresso.)</td>
</tr>
<tr class="even">
<td>formato de arquivo</td>
<td>Retorna o formato de arquivo atual para <a href="record.md">registrar ou</a> <strong>salvar</strong> comandos.</td>
</tr>
<tr class="odd">
<td>modo de arquivo</td>
<td>Retorna &quot; &quot; carregando , &quot; &quot; salvando , &quot; editando &quot; ou &quot; &quot; ocioso. Durante uma <a href="load.md"><strong>operação de</strong></a> carregamento, ele retorna o carregamento &quot; de &quot; . Durante <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>as operações de</strong></a> salvar <a href="capture.md"><strong>e</strong></a> capturar, ele retorna &quot; salvando &quot; . Durante as <a href="copy.md"><strong>operações</strong></a> <a href="cut.md"><strong>de recortar,</strong></a> <a href="delete.md"><strong></strong></a>copiar , excluir, <a href="paste.md"><strong>colar</strong></a>ou <a href="undo.md"><strong>desfazer,</strong></a> ele retorna a edição &quot; &quot; .</td>
</tr>
<tr class="even">
<td>format tag</td>
<td>Retorna a marca de formato.</td>
</tr>
<tr class="odd">
<td>avançar</td>
<td>Retornará <strong>TRUE</strong> se a direção da reprodução for para frente ou se o dispositivo não estiver sendo reproduzindo.</td>
</tr>
<tr class="even">
<td>taxa de quadros</td>
<td>Retorna o número de quadros por segundo que o dispositivo usará por padrão. Os dispositivos NTSC retornam 30, PAL 25 e assim por diante.</td>
</tr>
<tr class="odd">
<td>quadros ignorados</td>
<td>Retorna o número de quadros que não foram desenhados quando a última sequência AVI foi tocada. Esse sinalizador é reconhecido apenas pelo driver de vídeo digital MCIAVI. Ele se trata apenas da avaliação de desempenho; o valor de retorno é difícil de interpretar.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Retorna o valor definido com <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gama como &quot; <em>valor</em>.</td>
</tr>
<tr class="odd">
<td>índice</td>
<td>Retorna a exibição de índice atual. Para obter mais informações, consulte o <a href="set.md"><strong>comando set</strong></a> &quot; &quot; index.</td>
</tr>
<tr class="even">
<td>índice em</td>
<td>Retornará <strong>TRUE</strong> se o índice estiver.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Retorna o conjunto de entrada. Se um não estiver definido, o erro retornado indicará que qualquer dispositivo pode ser usado. Para dispositivos de vídeo digital, modifica o botão , o volume , o volume, o brilho, a cor , o contraste, o gama, a sharpness ou o sinalizador de tonalidade para que ele se aplique somente &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; à &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; entrada. Esse é o padrão ao monitorar a entrada.</td>
</tr>
<tr class="even">
<td>volume esquerdo</td>
<td>Retorna o conjunto de volumes para o canal de áudio esquerdo.</td>
</tr>
<tr class="odd">
<td>comprimento</td>
<td>Retorna o comprimento total da mídia, no formato de hora atual. Para arquivos PPQN, o comprimento é retornado em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh:mm:ss:ff</em>, em que <em>hh</em> é horas, <em>mm é</em> minutos, <em>ss</em> é segundos e <em>ff</em> é quadros. Para dispositivos VCR, o comprimento é de 2 horas (a menos que o comprimento tenha sido alterado explicitamente usando o <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>comando set).</strong></a></td>
</tr>
<tr class="even">
<td>número da faixa de <em>comprimento</em></td>
<td>Retorna o comprimento da faixa, em tempo ou quadros, especificado pelo <em>número</em>. Para arquivos PPQN, o comprimento é retornado em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh:mm:ss:ff</em>, em que <em>hh</em> é horas, <em>mm é</em> minutos, <em>ss</em> é segundos e <em>ff</em> é quadros.<br/></td>
</tr>
<tr class="odd">
<td>nível</td>
<td>Retorna o valor de exemplo de áudio PCM atual.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Retorna &quot; midi &quot; , nenhum ou &quot; &quot; &quot; smpte &quot; dependendo do tipo de conjunto de sincronização.</td>
</tr>
<tr class="odd">
<td>mídia presente</td>
<td>Retornará <strong>TRUE</strong> se a mídia for inserida no dispositivo ou <strong>FALSE</strong> caso contrário. Os dispositivos Sequencer, video-overlay, digital-video e waveform-audio <strong>retornam TRUE.</strong></td>
</tr>
<tr class="even">
<td>tipo de mídia</td>
<td>Retorna o tipo da mídia. Para VCRS, é &quot; 8mm &quot; , &quot; vhs &quot; , &quot; svhs &quot; , &quot; &quot; beta, &quot; Hi8 , &quot; &quot; edbeta &quot; ou outro &quot; &quot; . Para videodiscs, esse é &quot; o &quot; CID, CLV ou outro , &quot; &quot; &quot; &quot; dependendo do tipo de videodisc.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Retorna o modo atual do dispositivo. Todos os dispositivos podem retornar os &quot; valores &quot; não prontos, &quot; &quot; pausados, &quot; em reprodução e &quot; &quot; &quot; interrompidos. Alguns dispositivos podem retornar os valores &quot; abertos &quot; &quot; adicionais, revisando &quot; , &quot; &quot; gravando e buscando &quot; &quot; valores.</td>
</tr>
<tr class="even">
<td>monitor</td>
<td>Retorna &quot; o arquivo ou a entrada &quot; &quot; &quot; . O valor retornado indica a origem da apresentação atual.</td>
</tr>
<tr class="odd">
<td>método monitor</td>
<td>Retorna &quot; &quot; pré, &quot; post &quot; ou &quot; &quot; direto. O valor retornado indica o método usado para monitoramento de entrada.</td>
</tr>
<tr class="even">
<td>Nominal</td>
<td>O item modifica os sinalizadores de volume , brilho , cor , contraste , gama, a &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; sharpness &quot; , tint , treble e &quot; sinalizadores de volume &quot; &quot; &quot; &quot; &quot; para retornar o valor nominal em vez da configuração atual.</td>
</tr>
<tr class="odd">
<td>taxa de quadros nominal</td>
<td>Retorna a taxa de quadros nominal associada ao arquivo. As unidades estão em quadros por segundo multiplicados por 1000.</td>
</tr>
<tr class="even">
<td>taxa de quadros de registro nominal</td>
<td>Retorna a taxa de quadros nominal associada ao sinal de vídeo de entrada. As unidades estão em quadros por segundo multiplicados por 1000.</td>
</tr>
<tr class="odd">
<td>número de faixas de áudio</td>
<td>Retorna o número de faixas de áudio na mídia.</td>
</tr>
<tr class="even">
<td>número de faixas</td>
<td>Retorna o número de faixas na mídia. Os dispositivos MCISEQ e MCIWAVE retornam 1, assim como a maioria dos dispositivos VCR. O dispositivo MCIPIONR não dá suporte a esse sinalizador.</td>
</tr>
<tr class="odd">
<td>número de faixas de vídeo</td>
<td>Retorna o número de faixas de vídeo na mídia.</td>
</tr>
<tr class="even">
<td>deslocamento</td>
<td>Retorna o deslocamento de um arquivo baseado em SMPTE. O deslocamento é a hora de início de uma sequência baseada em SMPTE. O tempo é retornado como <em>hh:mm:ss:ff</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>ss</em> é segundos e <em>ff</em> é quadros.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Retorna a saída definida no momento. Se nenhuma saída for definida, o erro retornado indicará que qualquer dispositivo pode ser usado. Para dispositivos de vídeo digital, modifica o botão , o volume , o volume, o brilho, a cor , o &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; contraste, o &quot; &quot; gama, &quot; &quot; &quot; &quot; a sharpness ou o sinalizador de tonalidade para que ele se aplique somente à saída. Esse é o padrão ao monitorar um arquivo.</td>
</tr>
<tr class="even">
<td>modo de pausa</td>
<td>Retornará &quot; a gravação se o dispositivo estiver em pausa durante a &quot; gravação. Ele &quot; retornará a &quot; reprodução se o dispositivo estiver em pausa durante a reprodução. Ele retornará o erro &quot; Ação não aplicável no modo atual &quot; se o dispositivo não estiver em pausa.</td>
</tr>
<tr class="odd">
<td>tempo de pausa</td>
<td>Retorna a duração máxima, em milissegundos, de um <a href="pause.md"><strong>comando pause.</strong></a></td>
</tr>
<tr class="even">
<td>formato de reprodução</td>
<td>Retorna um código que indica o formato no qual o filme será tocado novamente, se detectável: &quot; lp , ep , sp ou outro &quot; &quot; &quot; &quot; &quot; &quot; &quot; . Para obter mais informações, consulte o &quot; sinalizador de formato de &quot; registro.</td>
</tr>
<tr class="odd">
<td>velocidade de reprodução</td>
<td>Retorna um valor que representa o quanto o tempo real de reprodução da última sequência AVI corresponderam ao tempo de reprodução de destino. O valor 1000 indica que a hora de destino e a hora real foram as mesmas. Um valor de 2000, por exemplo, indicaria que a sequência AVI demorou duas vezes mais tempo para ser reproduzida como deveria. Esse sinalizador é reconhecido apenas pelo driver de vídeo digital MCIAVI. Ele se trata apenas da avaliação de desempenho; o valor de retorno é difícil de interpretar.</td>
</tr>
<tr class="even">
<td>porta</td>
<td>Retorna o número da porta MIDI atribuído à sequência.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Retorna a posição atual. Para arquivos PPQN, a posição é retornada em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh:mm:ss:ff</em>, em que <em>hh</em> é horas, <em>mm é</em> minutos, ss é segundos e <em>ff</em> é quadros.<br/></td>
</tr>
<tr class="even">
<td>position start</td>
<td>Retorna a posição do início da mídia acessível.</td>
</tr>
<tr class="odd">
<td>número da faixa de <em>posição</em></td>
<td>Retorna a posição do início da faixa especificada pelo <em>número</em>. Para arquivos PPQN, o formato de hora é retornado em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh:mm:ss:ff</em>, em que <em>hh</em> é horas, <em>mm é</em> minutos, <em>ss</em> é segundos e <em>ff</em> é quadros. O sequenciador MCISEQ retorna zero. O dispositivo MCIPIONR não dá suporte a esse sinalizador. O dispositivo MCIWAVE retorna zero.</td>
</tr>
<tr class="even">
<td>duração do pós-roll</td>
<td>Retorna o comprimento da pausa, no formato de hora atual, necessário <a href="pause.md"><strong></strong></a> para interromper o transporte do VCR quando um comando <a href="stop.md"><strong>parar</strong></a> ou pausar é emitido.</td>
</tr>
<tr class="odd">
<td>power on</td>
<td>Retornará <strong>TRUE</strong> se a energia do VCR estiver íntegrada.</td>
</tr>
<tr class="even">
<td>duração do pré-roll</td>
<td>Retorna o comprimento da fita, no formato de hora atual, necessário para estabilizar a saída do VCR.</td>
</tr>
<tr class="odd">
<td>Pronto</td>
<td>Retornará <strong>TRUE</strong> se o dispositivo estiver pronto para aceitar outro comando.</td>
</tr>
<tr class="even">
<td>formato de registro</td>
<td>Retorna um código que indica o formato no qual a floresta será registrada. Os tipos de retorno atuais são &quot; &quot; lp, &quot; ep , sp ou outro &quot; &quot; &quot; &quot; &quot; . Esses formatos não são específicos do VHS e podem ser aplicados a qualquer VCR que tenha vários formatos de gravação selecionáveis. O tipo sp é o formato de gravação mais rápido e de alta qualidade e &quot; é usado como padrão em &quot; VCRs de formato único.</td>
</tr>
<tr class="odd">
<td>taxa de quadros de registro</td>
<td>Retorna a taxa de quadros, em quadros por segundo multiplicado por 1000, usada para compactação.</td>
</tr>
<tr class="even">
<td>quadro <em>de referência</em></td>
<td>Retorna o número do quadro para a imagem de quadro-chave mais próxima que precede o quadro <em>especificado.</em></td>
</tr>
<tr class="odd">
<td>tamanho reservado</td>
<td>Retorna o tamanho, no formato de hora atual, do workspace reservado. O tamanho corresponde ao tempo aproximado que levaria para reproduzir os dados compactados de um workspace completo. Ele retornará zero se não houver espaço em disco reservado. Esse sinalizador retorna o tamanho aproximado porque o espaço em disco preciso para dados compactados não pode, em geral, ser previsto até que os dados sejam compactados.</td>
</tr>
<tr class="even">
<td>volume à direita</td>
<td>Retorna o conjunto de volumes para o canal de áudio à direita.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Retorna o número de amostras por segundo tocadas ou gravadas.</td>
</tr>
<tr class="even">
<td>buscar exatamente</td>
<td>Retorna &quot; on ou off , &quot; indicando se o sinalizador de busca está definido &quot; ou &quot; &quot; &quot; não.</td>
</tr>
<tr class="odd">
<td>Nitidez</td>
<td>Retorna o nível de sharpness atual do dispositivo.</td>
</tr>
<tr class="even">
<td>Lado</td>
<td>Retorna 1 ou 2 para indicar qual lado do videodisc é carregado.</td>
</tr>
<tr class="odd">
<td>Escravo</td>
<td>Retorna &quot; o arquivo , &quot; &quot; midi , nenhum ou &quot; &quot; &quot; &quot; smpte &quot; dependendo do tipo de conjunto de sincronização.</td>
</tr>
<tr class="even">
<td>Smpte</td>
<td>Retorna o código de tempo SMPTE associado à posição atual no workspace. Essa é uma cadeia de caracteres com o formato <em>dd:dd:dd:dd</em>, em que cada <em>d</em> indica um dígito de 0 a 9. Se os dados do workspace não incluirem dados de código de data/hora, esse sinalizador retornará 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>velocidade</td>
<td>Retorna a velocidade atual do dispositivo em quadros por segundo (ou no mesmo formato usado pelo comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; &quot; speed). O player de videodisc MCIPIONR não dá suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td>posição inicial</td>
<td>Retorna a posição inicial da mídia.</td>
</tr>
<tr class="odd">
<td>formato de arquivo still</td>
<td>Retorna o formato de arquivo atual para o <a href="capture.md"><strong>comando de</strong></a> captura.</td>
</tr>
<tr class="even">
<td>Esticar</td>
<td>Retornará <strong>TRUE</strong> se o alongamento estiver habilitado.</td>
</tr>
<tr class="odd">
<td>tempo</td>
<td>Retorna o tempo atual de uma sequência MIDI no formato de hora atual. Para arquivos com formato PPQN, o tempo está em ritmos por minuto. Para arquivos com formato SMPTE, o tempo está em quadros por segundo.</td>
</tr>
<tr class="even">
<td>formato de tempo</td>
<td>Retorna o formato de hora atual. Para obter mais informações, consulte os formatos de hora no <a href="set.md"><strong>comando set.</strong></a></td>
</tr>
<tr class="odd">
<td>modo de tempo</td>
<td>Retorna o modo de tempo de posição atual. Ele pode ser &quot; detectar , o código de tempo ou o contador &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>tipo de tempo</td>
<td>Retorna o tempo de posição atual em uso: &quot; código de tempo ou contador &quot; &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>timecode present</td>
<td>Retornará <strong>TRUE</strong> se o código de hora tiver sido gravado na posição atual na fita. O código de tempo deve avançar da posição atual. Talvez seja necessário reproduzir um videocassete para verificar essa condição.</td>
</tr>
<tr class="even">
<td>registro de código de histórico</td>
<td>Retornará <strong>true</strong> se o VCR estiver definido para registrar o código de pafica.</td>
</tr>
<tr class="odd">
<td>tipo de código de Code</td>
<td>Retorna &quot; SMPTE &quot; , &quot; SMPTE Drop &quot; , &quot; outro &quot; ou &quot; nenhum &quot; . Observe que os quadros por segundo podem ser obtidos do comando de taxa de quadros de status &quot; &quot; e a precisão do dispositivo pode ser retornada pelo comando de precisão de busca de <a href="capability.md"><strong>funcionalidade</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Nuance</td>
<td>Retorna o nível de tonalidade de vídeo atual.</td>
</tr>
<tr class="odd">
<td>agudo</td>
<td>Retorna o nível de áudio-agudo atual.</td>
</tr>
<tr class="even">
<td>número do sintonizador</td>
<td>Retorna o número do sintonizador lógico atual.</td>
</tr>
<tr class="odd">
<td>não salvas</td>
<td>Retorna <strong>true</strong> se houver dados registrados no espaço de trabalho que podem ser perdidos como resultado de um comando <a href="close.md"><strong>Close</strong></a>, <a href="load.md"><strong>Load</strong></a>, <a href="record.md"><strong>Record</strong></a>, <a href="reserve.md"><strong>Reserve</strong></a>, <a href="cut.md"><strong>Cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>ou <a href="paste.md"><strong>Paste</strong></a> . Retorna <strong>false</strong> caso contrário.</td>
</tr>
<tr class="even">
<td>video</td>
<td>Retorna &quot; on &quot; ou &quot; off &quot; , refletindo o estado definido pelo comando <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="odd">
<td>cor da chave do vídeo</td>
<td>Retorna o valor da cor da chave.</td>
</tr>
<tr class="even">
<td>índice de chave de vídeo</td>
<td>Retorna o valor para o índice de chave.</td>
</tr>
<tr class="odd">
<td>monitor de vídeo</td>
<td>Retorna &quot; &quot; a saída ou um dos tipos de entrada de origem válidos. Para obter mais informações, consulte o comando monitor <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>número do monitor de vídeo</td>
<td>Retorna o número monitorado de vídeo do tipo retornado pelo monitor de vídeo de status &quot; &quot; . Para obter mais informações, consulte o comando <a href="setvideo.md">setvideo</a> .</td>
</tr>
<tr class="odd">
<td>registro de vídeo</td>
<td>Retorna &quot; ativado &quot; ou &quot; desativado &quot; , refletindo o estado atual definido pelo registro de conjunto de <a href="setvideo.md"><strong>vídeos</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>número</em> de faixa do registro de vídeo</td>
<td>Retornará <strong>true</strong> se o VCR estiver definido para gravar vídeo. Se nenhum número de faixa for fornecido, o valor padrão de 1 será assumido.</td>
</tr>
<tr class="odd">
<td>fonte de vídeo</td>
<td>Retorna o tipo de fonte de vídeo. Para obter mais informações, consulte o comando <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="even">
<td>número da fonte do vídeo</td>
<td>Retorna um número correspondente à fonte de vídeo do tipo em uso. Por exemplo, ele retornará 2 se a segunda entrada de fonte de vídeo NTSC estiver sendo usada.</td>
</tr>
<tr class="odd">
<td>fluxo de vídeo</td>
<td>Retorna o número do fluxo de vídeo atual.</td>
</tr>
<tr class="even">
<td>volume</td>
<td>Retorna o volume médio para o alto-falante esquerdo e direito. Isso retornará um erro se o dispositivo não tiver sido reproduzido ou se o volume não tiver sido definido.</td>
</tr>
<tr class="odd">
<td>identificador de janela</td>
<td>Retorna o valor decimal ASCII para o identificador de janela na palavra de ordem inferior do valor de retorno.</td>
</tr>
<tr class="even">
<td>janela maximizada</td>
<td>Retornará <strong>true</strong> se a janela for maximizada.</td>
</tr>
<tr class="odd">
<td>janela minimizada</td>
<td>Retornará <strong>true</strong> se a janela for minimizada.</td>
</tr>
<tr class="even">
<td>janela visível</td>
<td>Retornará <strong>true</strong> se a janela não estiver oculta.</td>
</tr>
<tr class="odd">
<td>protegido contra gravação</td>
<td>Retornará <strong>true</strong> se o dispositivo detectar que ele não pode gravar (ou seja, se a proteção contra gravação estiver ativada). Se ele puder gravar, ou se não for possível determinar se ele pode ou não gravar (sem realmente escrever), o driver retornará <strong>false</strong>.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna informações no parâmetro *lpszReturnString* de [**mciSendString**](/previous-versions//dd757161(v=vs.85)). As informações dependem do tipo de solicitação.

## <a name="remarks"></a>Comentários

Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .

## <a name="examples"></a>Exemplos

O comando a seguir retorna o modo atual do dispositivo "mysound".

``` syntax
status mysound mode
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

[capability](capability.md)
</dt> <dt>

[captura](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[migração](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[carga](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Olar](paste.md)
</dt> <dt>

[gravável](record.md)
</dt> <dt>

[reservado](reserve.md)
</dt> <dt>

[salvar](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[desfazer](undo.md)
</dt> </dl>

 

