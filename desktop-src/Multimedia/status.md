---
title: comando de status
description: O comando status solicita informações de status de um dispositivo. Todos os dispositivos reconhecem este comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando de status multimídia do Windows
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105759626"
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
<col style="width: 50%" />
<col style="width: 50%" />
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
<li>identificador de janela</li>
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
<li>esteja</li>
<li>Estendi</li>
<li>identificador de janela</li>
</ul></td>
</tr>
<tr class="even">
<td>sequenciador</td>
<td><ul>
<li>faixa atual</li>
<li>tipo de divisão</li>
<li>comprimento</li>
<li>comprimento mestre do <em>número</em> de faixas</li>
<li>mídia presente</li>
<li>mode</li>
<li>número de faixas</li>
<li>deslocamento</li>
<li>porta</li>
<li>position</li>
<li><em>número</em> da faixa de posição</li>
<li>esteja</li>
<li>subordinado</li>
<li>posição inicial</li>
<li>golpe</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="odd">
<td>videocassete</td>
<td><ul>
<li>montar registro</li>
<li>monitor de áudio</li>
<li>número do monitor de áudio</li>
<li>registro de áudio</li>
<li><em>número</em> de faixa do registro de áudio</li>
<li>fonte de áudio</li>
<li>número da fonte de áudio</li>
<li>channel</li>
<li><em>número</em> do sintonizador de canal</li>
<li>clock</li>
<li>ID do relógio</li>
<li>contador</li>
<li>formato do contador</li>
<li>resolução do contador</li>
<li>faixa atual</li>
<li>taxa de quadros</li>
<li>índice</li>
<li>índice ativado</li>
<li>comprimento</li>
<li><em>número</em> de faixa de comprimento</li>
<li>mídia presente</li>
<li>tipo de mídia</li>
<li>mode</li>
<li>número de faixas de áudio</li>
<li>número de faixas</li>
<li>número de faixas de vídeo</li>
<li><em>tempo limite</em> de pausa</li>
<li>formato de reprodução</li>
<li>position</li>
<li>início da posição</li>
<li><em>número</em> da faixa de posição</li>
<li><em>duração</em> do registro</li>
<li>ligar</li>
<li><em>duração</em> da preversão</li>
<li>esteja</li>
<li>formato de registro</li>
<li>velocidade</li>
<li>formato de hora</li>
<li>modo de tempo</li>
<li>tipo de hora</li>
<li>código de paficação presente</li>
<li>registro de código de histórico</li>
<li>tipo de código de Code</li>
<li>número do sintonizador</li>
<li>monitor de vídeo</li>
<li>número do monitor de vídeo</li>
<li>registro de vídeo</li>
<li><em>número</em> de faixa do registro de vídeo</li>
<li>fonte de vídeo</li>
<li>número da fonte do vídeo</li>
<li>protegido contra gravação</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>faixa atual</li>
<li>tamanho do disco</li>
<li>avançar</li>
<li>comprimento</li>
<li><em>número</em> de faixa de comprimento</li>
<li>mídia presente</li>
<li>tipo de mídia</li>
<li>mode</li>
<li>número de faixas</li>
<li>position</li>
<li><em>número</em> da faixa de posição</li>
<li>esteja</li>
<li>residente</li>
<li>velocidade</li>
<li>posição inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>alinhamento</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>canais</li>
<li>faixa atual</li>
<li>marca de formato</li>
<li>input</li>
<li>comprimento</li>
<li><em>número</em> de faixa de comprimento</li>
<li>nível</li>
<li>mídia presente</li>
<li>mode</li>
<li>número de faixas</li>
<li>output</li>
<li>position</li>
<li><em>número</em> da faixa de posição</li>
<li>esteja</li>
<li>samplespersec</li>
<li>posição inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRequest** e seus significados.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Retornará <strong>true</strong> se o dispositivo for definido para montar o modo de registro.</td>
</tr>
<tr class="odd">
<td>áudio</td>
<td>Retorna &quot; on &quot; ou &quot; off &quot; dependendo do comando mais recente <a href="setaudio.md"></a> &quot; de on &quot; ou off de &quot; áudio &quot; . Ele será &quot; retornado &quot; se um ou ambos os alto-falantes estiverem habilitados e &quot; fora do &quot; contrário.</td>
</tr>
<tr class="even">
<td>alinhamento de áudio</td>
<td>Retorna o alinhamento dos blocos de dados em relação ao início da entrada dados de formato de onda-áudio.</td>
</tr>
<tr class="odd">
<td>BitsPerSample de áudio</td>
<td>Retorna o número de bits por amostra que o dispositivo usa para gravação. Esse sinalizador se aplica somente a dispositivos que dão suporte ao &quot; &quot; algoritmo PCM.</td>
</tr>
<tr class="even">
<td>quebras de áudio</td>
<td>Retorna o número de vezes que a parte de áudio da última sequência AVI se quebrou. O sistema conta uma quebra de áudio sempre que tenta gravar dados de áudio no driver de dispositivo e descobre que o driver já reproduziu todos os dados disponíveis. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI. Ele destina-se apenas à avaliação de desempenho; o valor de retorno é difícil de interpretar.</td>
</tr>
<tr class="odd">
<td>bytespersec de áudio</td>
<td>Retorna o número médio de bytes por segundo usados para gravação.</td>
</tr>
<tr class="even">
<td>entrada de áudio</td>
<td>Retorna o nível de áudio instantâneo aproximado do sinal de áudio de entrada analógica. Um valor maior que 1000 implica distorção de recorte. Alguns dispositivos podem retornar esse valor somente durante a gravação de áudio. O valor não tem nenhum comando <a href="set.md">set</a> ou <a href="setaudio.md">SetAudio</a> associado.</td>
</tr>
<tr class="odd">
<td>monitor de áudio</td>
<td>Retorna &quot; &quot; a saída ou um dos tipos de entrada de origem válidos. Para obter mais informações, consulte o comando monitor <strong>SetAudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>número do monitor de áudio</td>
<td>Retorna o número monitorado de vídeo do tipo especificado pelo monitor de áudio de <strong>status</strong> &quot; &quot; . Para obter mais informações, consulte o comando <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="odd">
<td>registro de áudio</td>
<td>Retorna &quot; on &quot; ou &quot; off &quot; , refletindo o estado definido pelo registro de conjunto de <strong>áudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>número</em> de faixa do registro de áudio</td>
<td>Retornará <strong>true</strong> se o VCR estiver definido para gravar áudio. Se nenhum número de faixa for fornecido, o valor padrão de 1 será assumido.</td>
</tr>
<tr class="odd">
<td>samplespersec de áudio</td>
<td>Retorna o número de amostras por segundo registradas.</td>
</tr>
<tr class="even">
<td>fonte de áudio</td>
<td>Retorna a fonte do digitalizador de áudio atual: &quot; esquerda &quot; , &quot; direita &quot; , &quot; média &quot; ou &quot; estéreo &quot; .</td>
</tr>
<tr class="odd">
<td>número da fonte de áudio</td>
<td>Retorna o número da fonte de áudio do tipo retornado pela fonte de áudio de <strong>status</strong> &quot; &quot; . Para obter mais informações, consulte o comando <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="even">
<td>fluxo de áudio</td>
<td>Retorna o número do fluxo de áudio atual.</td>
</tr>
<tr class="odd">
<td>graves</td>
<td>Retorna o nível de áudio-Bass atual.</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>Retorna o número de bits por pixel para salvar dados capturados ou gravados.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Retorna os bits por amostra.</td>
</tr>
<tr class="even">
<td>lo</td>
<td>Retorna o nível de brilho do vídeo atual.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Retorna o número médio de bytes por segundo reproduzidos ou gravados.</td>
</tr>
<tr class="even">
<td><em>número</em> de faixa do tipo cdaudio</td>
<td>Retorna o tipo do número de faixa especificado. Pode ser &quot; áudio &quot; ou &quot; outros.&quot;</td>
</tr>
<tr class="odd">
<td>channel</td>
<td>Retorna o valor inteiro do conjunto de canais no sintonizador.</td>
</tr>
<tr class="even">
<td><em>número</em> do sintonizador de canal</td>
<td>Se &quot; o &quot; <em>número</em> do sintonizador for fornecido, o canal selecionado no momento no <em>número</em> do sintonizador lógico será retornado. Observe que pode haver vários sintonizadores lógicos.</td>
</tr>
<tr class="odd">
<td>canais</td>
<td>Retorna o número de canais definido (1 para mono, 2 para estéreo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Retorna o tempo externo. O tempo deve ser um inteiro longo não assinado que expresse incrementos totais. Para obter mais informações, consulte o comando de taxa de incremento de relógio de <a href="capability.md">funcionalidade</a> &quot; &quot; .</td>
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
<td>Retorna a posição do contador, no formato do contador atual.</td>
</tr>
<tr class="odd">
<td>formato do contador</td>
<td>Retorna o formato do contador atual. Para obter mais informações, consulte o comando <a href="set.md">set</a> &quot; Counter Format &quot; .</td>
</tr>
<tr class="even">
<td>resolução do contador</td>
<td>Retorna &quot; quadros &quot; ou &quot; segundos &quot; , indicando a resolução do contador. Isso não é o mesmo que precisão.</td>
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
<td><em>unidade</em> de espaço em disco</td>
<td>Retorna o espaço em disco aproximado, no formato de hora atual, que pode ser obtido por um comando de <a href="reserve.md">reserva</a> para a unidade de disco especificada <em>.</em> A <em>unidade</em> geralmente é especificada como uma única letra ou uma única letra seguida por dois-pontos (:). Alguns dispositivos, no entanto, podem usar um caminho.</td>
</tr>
<tr class="even">
<td>tipo de divisão</td>
<td>Retorna um dos seguintes tipos de divisão de arquivo:
<ul>
<li>PPQN</li>
<li>Quadro SMPTE 24</li>
<li>Quadro SMPTE 25</li>
<li>Quadro suspenso SMPTE 30</li>
<li>Quadro SMPTE 30</li>
</ul>
<br/> Use essas informações para determinar o formato do arquivo MIDI e o significado das informações de tempo e de posição.<br/></td>
</tr>
<tr class="odd">
<td>conclusão do arquivo</td>
<td>Retorna a porcentagem estimada em que uma operação de <a href="load.md">carregamento</a>, <a href="save.md">gravação</a>, <a href="capture.md">captura</a>, <a href="cut.md">recorte</a>, <a href="copy.md">cópia</a>, <a href="delete.md">exclusão</a>, <a href="paste.md">colagem</a>ou <a href="undo.md">desfazer</a> foi progredida. (Os aplicativos podem usar isso para fornecer um indicador visual de progresso.)</td>
</tr>
<tr class="even">
<td>formato de arquivo</td>
<td>Retorna o formato de arquivo atual para <a href="record.md">gravar</a> ou <strong>salvar</strong> comandos.</td>
</tr>
<tr class="odd">
<td>modo de arquivo</td>
<td>Retorna o &quot; carregamento, a gravação, a &quot; &quot; &quot; &quot; edição ou a &quot; &quot; ociosidade &quot; . Durante uma operação de <a href="load.md"><strong>carregamento</strong></a> , ele retorna o &quot; carregamento &quot; . Durante as operações de <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>salvar</strong></a> e <a href="capture.md"><strong>capturar</strong></a> , ele retorna &quot; salvando &quot; . Durante as operações <a href="cut.md"><strong>recortar</strong></a>, <a href="copy.md"><strong>copiar</strong></a>, <a href="delete.md"><strong>excluir</strong></a>, <a href="paste.md"><strong>colar</strong></a>ou <a href="undo.md"><strong>desfazer</strong></a> , ela retorna &quot; edição &quot; .</td>
</tr>
<tr class="even">
<td>marca de formato</td>
<td>Retorna a marca de formato.</td>
</tr>
<tr class="odd">
<td>avançar</td>
<td>Retornará <strong>true</strong> se a direção de reprodução for encaminhada ou se o dispositivo não estiver sendo reproduzido.</td>
</tr>
<tr class="even">
<td>taxa de quadros</td>
<td>Retorna o número de quadros por segundo que o dispositivo usará por padrão. Os dispositivos NTSC retornam 30, PAL 25 e assim por diante.</td>
</tr>
<tr class="odd">
<td>quadros ignorados</td>
<td>Retorna o número de quadros que não foram desenhados quando a última sequência AVI foi reproduzida. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI. Ele destina-se apenas à avaliação de desempenho; o valor de retorno é difícil de interpretar.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Retorna o valor definido com <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gama para &quot; <em>valor</em>.</td>
</tr>
<tr class="odd">
<td>índice</td>
<td>Retorna a exibição do índice atual. Para obter mais informações, consulte o comando <a href="set.md"><strong>set</strong></a> &quot; index &quot; .</td>
</tr>
<tr class="even">
<td>índice ativado</td>
<td>Retornará <strong>true</strong> se o índice estiver ativado.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Retorna o conjunto de entrada. Se um não for definido, o erro retornado indica que qualquer dispositivo pode ser usado. Para dispositivos de vídeo digital, o modifica os &quot; graves &quot; , os &quot; agudos &quot; , o &quot; volume, o &quot; &quot; brilho, a &quot; &quot; cor, o &quot; contraste, o gama, a &quot; &quot; &quot; &quot; &quot; nitidez ou o sinalizador de &quot; &quot; tonalidade &quot; para que ele se aplique somente à entrada. Esse é o padrão ao monitorar a entrada.</td>
</tr>
<tr class="even">
<td>volume esquerdo</td>
<td>Retorna o conjunto de volumes para o canal de áudio à esquerda.</td>
</tr>
<tr class="odd">
<td>comprimento</td>
<td>Retorna o comprimento total da mídia, no formato de hora atual. Para arquivos PPQN, o comprimento é retornado em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames. Para dispositivos VCR, o comprimento é de 2 horas (a menos que o comprimento tenha sido explicitamente alterado usando o comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> ).</td>
</tr>
<tr class="even">
<td><em>número</em> de faixa de comprimento</td>
<td>Retorna o comprimento da faixa, em tempo ou quadros, especificado pelo <em>número</em>. Para arquivos PPQN, o comprimento é retornado em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.<br/></td>
</tr>
<tr class="odd">
<td>nível</td>
<td>Retorna o valor de exemplo de áudio PCM atual.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Retorna &quot; MIDI &quot; , &quot; None &quot; ou &quot; SMPTE, &quot; dependendo do tipo de sincronização definida.</td>
</tr>
<tr class="odd">
<td>mídia presente</td>
<td>Retornará <strong>true</strong> se a mídia for inserida no dispositivo ou <strong>false</strong> caso contrário. Os dispositivos Sequencer, vídeo-Overlay, digital-video e Wave-Audio retornam <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>tipo de mídia</td>
<td>Retorna o tipo da mídia. Para VCRS, isso é &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; ou &quot; outros &quot; . Para videodiscs, isso é &quot; CAV &quot; , &quot; CLV &quot; ou &quot; outro &quot; , dependendo do tipo de VIDEODISC.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Retorna o modo atual do dispositivo. Todos os dispositivos podem retornar os &quot; valores não prontos &quot; , &quot; &quot; em pausa, &quot; &quot; em execução e &quot; parado &quot; . Alguns dispositivos podem retornar os &quot; valores adicionais abrir &quot; , &quot; estacionados &quot; , de &quot; gravação e de &quot; &quot; busca &quot; .</td>
</tr>
<tr class="even">
<td>monitor</td>
<td>Retorna o &quot; arquivo &quot; ou a &quot; entrada &quot; . O valor retornado indica a fonte da apresentação atual.</td>
</tr>
<tr class="odd">
<td>método de monitor</td>
<td>Retorna &quot; pre &quot; , &quot; post &quot; ou &quot; Direct &quot; . O valor retornado indica o método usado para o monitoramento de entrada.</td>
</tr>
<tr class="even">
<td>nominal</td>
<td>O item modifica os &quot; graves &quot; , &quot; brilho &quot; , &quot; cor &quot; , &quot; contraste &quot; , &quot; gama &quot; , &quot; nitidez &quot; , &quot; tonalidade &quot; , &quot; agudos &quot; e sinalizadores de &quot; volume &quot; para retornar o valor nominal em vez da configuração atual.</td>
</tr>
<tr class="odd">
<td>taxa de quadros nominal</td>
<td>Retorna a taxa de quadros nominal associada ao arquivo. As unidades estão em quadros por segundo multiplicadas por 1000.</td>
</tr>
<tr class="even">
<td>taxa de quadros de registro nominal</td>
<td>Retorna a taxa de quadros nominal associada ao sinal de vídeo de entrada. As unidades estão em quadros por segundo multiplicadas por 1000.</td>
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
<td>Retorna o deslocamento de um arquivo baseado em SMPTE. O deslocamento é a hora de início de uma sequência baseada em SMPTE. O tempo é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Retorna a saída definida atualmente. Se nenhuma saída for definida, o erro retornado indica que qualquer dispositivo pode ser usado. Para dispositivos de vídeo digital, o modifica os &quot; graves &quot; , os &quot; agudos &quot; , o &quot; volume, o &quot; &quot; brilho, a &quot; &quot; cor, o &quot; contraste, o gama, a &quot; &quot; &quot; &quot; &quot; nitidez ou o sinalizador de &quot; &quot; tonalidade &quot; para que ele se aplique somente à saída. Esse é o padrão ao monitorar um arquivo.</td>
</tr>
<tr class="even">
<td>modo de pausa</td>
<td>Retornará &quot; &quot; a gravação se o dispositivo estiver em pausa durante a gravação. Ele retornará a &quot; reprodução &quot; se o dispositivo estiver em pausa durante a reprodução. Ele retornará a ação de erro &quot; não aplicável no modo atual &quot; se o dispositivo não estiver em pausa.</td>
</tr>
<tr class="odd">
<td>tempo limite de pausa</td>
<td>Retorna a duração máxima, em milissegundos, de um comando de <a href="pause.md"><strong>pausa</strong></a> .</td>
</tr>
<tr class="even">
<td>formato de reprodução</td>
<td>Retorna um código que indica o formato em que a fita de vídeo será reproduzida, se detectável: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; outro &quot; . Para obter mais informações, consulte o &quot; sinalizador de formato de registro &quot; .</td>
</tr>
<tr class="odd">
<td>velocidade de reprodução</td>
<td>Retorna um valor que representa a precisão da hora de execução real da última sequência AVI correspondente ao tempo de execução de destino. O valor 1000 indica que a hora de destino e a hora real foram as mesmas. Um valor de 2000, por exemplo, indicaria que a sequência AVI levou duas vezes mais tempo que deveria ter. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI. Ele destina-se apenas à avaliação de desempenho; o valor de retorno é difícil de interpretar.</td>
</tr>
<tr class="even">
<td>porta</td>
<td>Retorna o número da porta MIDI atribuído à sequência.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Retorna a posição atual. Para arquivos PPQN, a posição é retornada em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, SS é segundos e <em>FF</em> é frames.<br/></td>
</tr>
<tr class="even">
<td>início da posição</td>
<td>Retorna a posição do início da mídia utilizável.</td>
</tr>
<tr class="odd">
<td><em>número</em> da faixa de posição</td>
<td>Retorna a posição do início da faixa especificada pelo <em>número</em>. Para arquivos PPQN, o formato de hora é retornado em unidades de ponteiro de música. Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames. O sequenciador MCISEQ retorna zero. O dispositivo MCIPIONR não dá suporte a esse sinalizador. O dispositivo MCIWAVE retorna zero.</td>
</tr>
<tr class="even">
<td>duração do registro</td>
<td>Retorna o comprimento da fita de vídeo, no formato de hora atual, necessário para <a href="stop.md"><strong>finalizar</strong></a> o transporte de videocassete quando um comando Stop ou <a href="pause.md"><strong>Pause</strong></a> é emitido.</td>
</tr>
<tr class="odd">
<td>ligar</td>
<td>Retornará <strong>true</strong> se a energia do VCR estiver ativada.</td>
</tr>
<tr class="even">
<td>duração da preversão</td>
<td>Retorna o comprimento da fita de vídeo, no formato de hora atual, necessário para estabilizar a saída de videocassete.</td>
</tr>
<tr class="odd">
<td>esteja</td>
<td>Retornará <strong>true</strong> se o dispositivo estiver pronto para aceitar outro comando.</td>
</tr>
<tr class="even">
<td>formato de registro</td>
<td>Retorna um código que indica o formato em que a fita de vídeo será gravada. Os tipos de retorno atuais são &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; outros &quot; . Esses formatos não são específicos de VHS e podem ser aplicados a qualquer VCR que tenha vários formatos de gravação selecionáveis. O &quot; tipo de SP &quot; é o formato de gravação mais rápido e de mais alta qualidade e é usado como padrão em VCRs de formato único.</td>
</tr>
<tr class="odd">
<td>taxa de quadros de registro</td>
<td>Retorna a taxa de quadros, em quadros por segundo, multiplicado por 1000, usado para compactação.</td>
</tr>
<tr class="even">
<td><em>quadro</em> de referência</td>
<td>Retorna o número do quadro da imagem do quadro de chave mais próxima que precede o <em>quadro</em>especificado.</td>
</tr>
<tr class="odd">
<td>Tamanho reservado</td>
<td>Retorna o tamanho, no formato de hora atual, do espaço de trabalho reservado. O tamanho corresponde ao tempo aproximado que levaria para reproduzir os dados compactados de um espaço de trabalho completo. Ele retornará zero se não houver espaço reservado em disco. Esse sinalizador retorna o tamanho aproximado porque o espaço em disco preciso para dados compactados não pode, em geral, ser previsto até que os dados sejam compactados.</td>
</tr>
<tr class="even">
<td>volume correto</td>
<td>Retorna o conjunto de volumes para o canal de áudio correto.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Retorna o número de amostras por segundo reproduzidas ou registradas.</td>
</tr>
<tr class="even">
<td>buscar exatamente</td>
<td>Retorna &quot; on &quot; ou &quot; off &quot; , indicando se o sinalizador de &quot; busca exata &quot; está ou não definido.</td>
</tr>
<tr class="odd">
<td>nitidez</td>
<td>Retorna o nível de nitidez atual do dispositivo.</td>
</tr>
<tr class="even">
<td>residente</td>
<td>Retorna 1 ou 2 para indicar qual lado do VIDEODISC é carregado.</td>
</tr>
<tr class="odd">
<td>subordinado</td>
<td>Retorna &quot; arquivo &quot; , &quot; MIDI &quot; , &quot; nenhum &quot; ou &quot; SMPTE, &quot; dependendo do tipo de sincronização definido.</td>
</tr>
<tr class="even">
<td>SMPTE</td>
<td>Retorna o código de tempo SMPTE associado à posição atual no espaço de trabalho. Esta é uma cadeia de caracteres com o formato <em>DD: DD: DD: DD</em>, em que cada <em>d</em> denota um dígito de 0 a 9. Se os dados do espaço de trabalho não incluírem dados de código de data, esse sinalizador retornará 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>velocidade</td>
<td>Retorna a velocidade atual do dispositivo em quadros por segundo (ou no mesmo formato usado pelo comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; Speed &quot; ). O MCIPIONR VIDEODISC Player não dá suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td>posição inicial</td>
<td>Retorna a posição inicial da mídia.</td>
</tr>
<tr class="odd">
<td>formato de arquivo ainda</td>
<td>Retorna o formato de arquivo atual para o comando de <a href="capture.md"><strong>captura</strong></a> .</td>
</tr>
<tr class="even">
<td>Estendi</td>
<td>Retornará <strong>true</strong> se o alongamento estiver habilitado.</td>
</tr>
<tr class="odd">
<td>golpe</td>
<td>Retorna o tempo atual de uma sequência de MIDI no formato de hora atual. Para arquivos com o formato PPQN, o tempo é em batidas por minuto. Para arquivos com formato SMPTE, o tempo é em quadros por segundo.</td>
</tr>
<tr class="even">
<td>formato de hora</td>
<td>Retorna o formato de hora atual. Para obter mais informações, consulte os formatos de hora no comando <a href="set.md"><strong>set</strong></a> .</td>
</tr>
<tr class="odd">
<td>modo de tempo</td>
<td>Retorna o modo de tempo de posição atual. Ele pode ser &quot; detectado &quot; , &quot; código &quot; de Code ou &quot; contador &quot; .</td>
</tr>
<tr class="even">
<td>tipo de hora</td>
<td>Retorna o tempo de posição atual em uso: &quot; código &quot; de hora ou &quot; contador &quot; .</td>
</tr>
<tr class="odd">
<td>código de paficação presente</td>
<td>Retorna <strong>true</strong> se o código de tempo tiver sido registrado na posição atual na fita. O código de tempo deve avançar da posição atual. Talvez seja necessário reproduzir um videocassete para verificar essa condição.</td>
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

 

