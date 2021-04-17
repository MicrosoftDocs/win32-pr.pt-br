---
title: comando Set
description: O comando Set estabelece configurações de controle para o dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- definir o comando multimídia do Windows
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105770156"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dispositivo</th>
<th>Sinalizadores de comando</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li>porta fechada</li>
<li>porta aberta</li>
<li>milissegundos de formato de hora</li>
<li>meio do formato de hora MSF</li>
<li>tmsf de formato de hora</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li>porta fechada</li>
<li>porta aberta</li>
<li><em>formato</em> de formato de arquivo</li>
<li>buscar exatamente em</li>
<li>busca exata</li>
<li><em>fator</em> de velocidade</li>
<li><em>formato</em> de formato de arquivo ainda</li>
<li>quadros de formato de hora</li>
<li>milissegundos de formato de hora</li>
<li>vídeo desativado</li>
<li>vídeo ativado</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li>porta fechada</li>
<li>porta aberta</li>
<li>vídeo desativado</li>
<li>vídeo ativado</li>
</ul></td>
</tr>
<tr class="even">
<td>sequenciador</td>
<td><ul>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li>porta fechada</li>
<li>porta aberta</li>
<li>MIDI mestre</li>
<li>Mestre nenhum</li>
<li>Mestre SMPTE</li>
<li><em>tempo</em> de deslocamento</li>
<li>mapeador de porta</li>
<li>porta nenhum</li>
<li><em>port_number</em> de porta</li>
<li>arquivo subordinado</li>
<li>MIDI escravo</li>
<li>nenhum subordinado</li>
<li>SMPTE-escravo</li>
<li>tempo <em>tempo_value</em></li>
<li>milissegundos de formato de hora</li>
<li>formato de hora SMPTE <em>FPS</em></li>
<li>drop de formato de hora SMPTE 30</li>
<li>ponteiro de música de formato de hora</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>videocassete</strong></td>
<td><ul>
<li>montar registro em</li>
<li>montar registro</li>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li><em>hora</em> do relógio</li>
<li>formato do contador</li>
<li><em>valor</em> do contador</li>
<li>porta fechada</li>
<li>porta aberta</li>
<li>contador de índice</li>
<li>data do índice</li>
<li>hora do índice</li>
<li>hora do índice</li>
<li><em>duração</em> de CodeLength</li>
<li><em>tempo limite</em> de pausa</li>
<li>duração do registro-</li>
<li><em>duration</em></li>
<li>ligar</li>
<li>desligar</li>
<li><em>duração</em> da duração da preversão</li>
<li>formato de registro SP</li>
<li>formato de registro LP</li>
<li>formato de registro EP</li>
<li><em>fator</em> de velocidade</li>
<li>quadros de formato de hora</li>
<li>HMS de formato de hora</li>
<li>milissegundos de formato de hora</li>
<li>meio do formato de hora MSF</li>
<li>formato de hora SMPTE <em>FPS</em></li>
<li>drop de formato de hora SMPTE 30</li>
<li>tmsf de formato de hora</li>
<li>contador de modo de tempo</li>
<li>detecção de modo de tempo</li>
<li>tempo de vida de modo de hora</li>
<li>acompanhamento de mais</li>
<li>menos controle</li>
<li>redefinição de rastreamento</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li>porta fechada</li>
<li>porta aberta</li>
<li>quadros de formato de hora</li>
<li>HMS de formato de hora</li>
<li>milissegundos de formato de hora</li>
<li>faixa de formato de hora</li>
<li>vídeo desativado</li>
<li>vídeo ativado</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li><em>inteiro</em> de alinhamento</li>
<li>qualquer entrada</li>
<li>qualquer saída</li>
<li>áudio desativado</li>
<li>áudio tudo ativado</li>
<li>áudio restante</li>
<li>áudio restante em</li>
<li>áudio à direita</li>
<li>áudio à direita</li>
<li><em>bit_count</em> BitsPerSample</li>
<li><em>byte_rate</em> bytespersec</li>
<li>canais <em>channel_count</em></li>
<li>porta fechada</li>
<li>porta aberta</li>
<li>formato PCM de marca</li>
<li>Formatar <em>marca</em> de marca</li>
<li><em>número inteiro</em> de entrada</li>
<li><em>número inteiro</em> de saída</li>
<li>samplespersec <em>inteiro</em></li>
<li>bytes de formato de hora</li>
<li>milissegundos de formato de hora</li>
<li>exemplos de formato de hora</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszSetting** e seus significados.



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
<td><em>inteiro</em> de alinhamento</td>
<td>Define o alinhamento dos blocos de dados em relação ao início dos dados passados para o dispositivo de forma de onda-áudio. O arquivo é salvo neste formato.</td>
</tr>
<tr class="even">
<td>qualquer entrada</td>
<td>Use qualquer entrada que dê suporte ao formato atual durante a gravação. Essa é a configuração padrão.</td>
</tr>
<tr class="odd">
<td>qualquer saída</td>
<td>Use qualquer saída que dê suporte ao formato atual durante a execução. Esse é o padrão.</td>
</tr>
<tr class="even">
<td>montar registro em <br/> montar registro <br/></td>
<td>No modo de montagem, todas as faixas são registradas conforme definido pelo dispositivo. A maioria dos VCRs estão no modo de montagem por padrão.</td>
</tr>
<tr class="odd">
<td>áudio desativado <br/> áudio tudo ativado <br/></td>
<td>Desabilita ou habilita a saída de áudio. Dispositivos de sobreposição de vídeo, o sequenciador MCISEQ e o dispositivo MCIWAVE de onda-áudio não dão suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td>áudio restante <br/> áudio restante em <br/> áudio à direita <br/> áudio à direita <br/></td>
<td>Desabilita ou habilita a saída para o canal de áudio à esquerda ou à direita. Dispositivos de sobreposição de vídeo, o sequenciador MCISEQ e o dispositivo MCIWAVE de onda-áudio não dão suporte a esse sinalizador.</td>
</tr>
<tr class="odd">
<td><em>bit_count</em> BitsPerSample</td>
<td>Define o número de bits por amostra do PCM (modulação de código de pulso) reproduzido ou registrado. O arquivo é salvo neste formato.</td>
</tr>
<tr class="even">
<td><em>byte_rate</em> bytespersec</td>
<td>Define o número médio de bytes por segundo reproduzidos ou registrados. O arquivo é salvo neste formato.</td>
</tr>
<tr class="odd">
<td>canais <em>channel_count</em></td>
<td>Define os canais para reprodução e gravação. O arquivo é salvo neste formato.</td>
</tr>
<tr class="even">
<td><em>hora</em> do relógio</td>
<td>Define a hora no relógio externo para a <em>hora.</em> O formato é especificado como um inteiro não assinado longo.</td>
</tr>
<tr class="odd">
<td>formato do contador</td>
<td>Defina o formato de hora para o contador, conforme retornado pelo contador de <a href="status.md">status</a> &quot; &quot; . Para obter informações sobre os tipos aplicáveis, consulte o comando <strong>set</strong> &quot; Time Format &quot; .</td>
</tr>
<tr class="even">
<td><em>valor</em> do contador</td>
<td>Define o contador de VCR para o valor especificado. O valor deve ser especificado no formato de contador atual. Para obter mais informações, consulte o comando <strong>set</strong> &quot; Counter Format &quot; .</td>
</tr>
<tr class="odd">
<td>porta fechada</td>
<td>Cancela a bandeja e fecha a porta, se possível. Para VCRs, o carrega a fita automaticamente.</td>
</tr>
<tr class="even">
<td>porta aberta</td>
<td>Abre a porta e ejeta a bandeja ou fita, se possível.</td>
</tr>
<tr class="odd">
<td><em>formato</em> de formato de arquivo</td>
<td>Especifica um formato de arquivo que é usado para <a href="save.md">salvar</a> ou <a href="capture.md">capturar</a> comandos. Se omitido, isso pode padronizar para um formato definido por driver de dispositivo. Se o formato de arquivo especificado estiver em conflito com o algoritmo e a qualidade selecionados no momento, eles serão alterados para os padrões para o formato de arquivo. Os seguintes formatos de arquivo são definidos:
<ul>
<li>AVI: especifica o formato AVI.</li>
<li>avss: especifica o formato AVSS.</li>
<li>DIB: especifica o formato DIB.</li>
<li>JFIF: especifica o formato JFIF.</li>
<li>JPEG: especifica o formato JPEG.</li>
<li>MPEG: especifica o formato MPEG.</li>
<li>rdib: especifica o formato de DIB RLE.</li>
<li>rjpeg: especifica o formato RJPEG.</li>
</ul></td>
</tr>
<tr class="even">
<td>formato PCM de marca</td>
<td>Define o tipo de formato como PCM para reprodução e gravação. O arquivo é salvo neste formato.</td>
</tr>
<tr class="odd">
<td>Formatar <em>marca</em> de marca</td>
<td>Define o tipo de formato para reprodução e gravação. O arquivo é salvo neste formato.</td>
</tr>
<tr class="even">
<td>índice de código de <br/> contador de índice <br/> data do índice <br/> hora do índice <br/></td>
<td>Define a tela de exibição atual no VCR.</td>
</tr>
<tr class="odd">
<td><em>número inteiro</em> de entrada</td>
<td>Define o canal de áudio usado como entrada.</td>
</tr>
<tr class="even">
<td><em>duração</em> do comprimento</td>
<td>Define o comprimento especificado pelo usuário da fita no VCR. Esse comprimento é retornado pelo comando <a href="status.md">status</a> &quot; length &quot; e é fornecido para compatibilidade com aplicativos que exigem esse comando para retornar um comprimento válido.</td>
</tr>
<tr class="odd">
<td>MIDI mestre</td>
<td>Define o sequenciador MIDI como a origem da sincronização. Os dados de sincronização são enviados no formato MIDI. O sequenciador MCISEQ não dá suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td>Mestre nenhum</td>
<td>Inibe o sequenciador MIDI de enviar dados de sincronização. O sequenciador MCISEQ não dá suporte a esse sinalizador.</td>
</tr>
<tr class="odd">
<td>Mestre SMPTE</td>
<td>Define o sequenciador MIDI como a origem da sincronização. Os dados de sincronização são enviados em formato SMPTE (sociedade de imagem e engenheiros de televisão). O sequenciador MCISEQ não dá suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td><em>tempo</em> de deslocamento</td>
<td>Define o <em>tempo</em>de deslocamento SMPTE. O deslocamento é a hora de início de uma sequência baseada em SMPTE. O <em>tempo</em> é expresso como <em>hh</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, em que <em>hh</em> é hours, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</td>
</tr>
<tr class="odd">
<td><em>número inteiro</em> de saída</td>
<td>Define o canal de áudio usado como a saída.</td>
</tr>
<tr class="even">
<td><em>tempo limite</em> de pausa</td>
<td>Define a duração máxima, em milissegundos, de um comando de <a href="pause.md">pausa</a> . Um valor de <em>tempo limite</em> igual a zero indica que nenhum tempo limite ocorrerá.</td>
</tr>
<tr class="odd">
<td><em>duração</em> da duração do registro</td>
<td>Define o comprimento, no formato de hora atual, necessário para <a href="stop.md">finalizar</a> o transporte de videocassete quando um comando Stop ou <strong>Pause</strong> é emitido.</td>
</tr>
<tr class="even">
<td>mapeador de porta</td>
<td>Define o mapeador de MIDI como a porta que recebe as mensagens de MIDI. Esse comando falhará se o mapeador de MIDI ou uma porta necessária estiver sendo usado por outro aplicativo.</td>
</tr>
<tr class="odd">
<td>porta nenhum</td>
<td>Desabilita o envio de mensagens MIDI. Esse comando também fecha uma porta MIDI.</td>
</tr>
<tr class="even">
<td><em>port_number</em> de porta</td>
<td>Define a porta MIDI que recebe as mensagens MIDI. Esse comando falhará se a porta que você está tentando abrir estiver sendo usada por outro aplicativo.</td>
</tr>
<tr class="odd">
<td>ligar <br/> desligar <br/></td>
<td>Define a energia do dispositivo como on ou off.</td>
</tr>
<tr class="even">
<td><em>duração</em> da duração da preversão</td>
<td>Define o comprimento, no formato de hora atual, necessário para estabilizar a saída de VCR.</td>
</tr>
<tr class="odd">
<td>formato de registro SP <br/> formato de registro LP <br/> formato de registro EP <br/></td>
<td>Define o modo de gravação para o VCR para o SP para Play Standard, EP para reprodução estendida ou LP para reprodução longa. Esses valores não se destinam a ser específicos de VHS. Eles são mapeados para quaisquer três modos apropriados com outros formatos de fita. Por exemplo, o SP é mapeado para a gravação mais rápida e de qualidade mais alta.</td>
</tr>
<tr class="even">
<td>samplespersec <em>inteiro</em></td>
<td>Define a taxa de amostra para reprodução e gravação. O arquivo é salvo neste formato.</td>
</tr>
<tr class="odd">
<td>buscar exatamente em<br/> busca exata <br/></td>
<td>Seleciona um dos dois modos de busca. Com &quot; o Seek exactly on &quot; , Seek sempre será movido para o quadro especificado. Com &quot; Seek exactly off &quot; , Seek passará para o quadro-chave mais próximo antes do quadro especificado.</td>
</tr>
<tr class="even">
<td>arquivo subordinado</td>
<td>Define o sequenciador MIDI para usar dados de arquivo como a origem da sincronização. Essa é a configuração padrão.</td>
</tr>
<tr class="odd">
<td>MIDI escravo</td>
<td>Define o sequenciador MIDI para usar dados MIDI de entrada para a origem de sincronização. O Sequencer reconhece os dados de sincronização com o formato MIDI. O sequenciador MCISEQ não dá suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td>nenhum subordinado</td>
<td>Define o sequenciador MIDI para ignorar a sincronização</td>
</tr>
<tr class="odd">
<td>SMPTE-escravo</td>
<td>Define o sequenciador MIDI para usar dados MIDI de entrada para a origem de sincronização. O Sequencer reconhece os dados de sincronização com o formato SMPTE. O sequenciador MCISEQ não dá suporte a esse sinalizador.</td>
</tr>
<tr class="even">
<td>fator de velocidade</td>
<td>Define a velocidade relativa de reprodução de áudio e vídeo do espaço de trabalho. Factor é a proporção entre a taxa de quadros nominal e a taxa de quadros desejada, em que a taxa de quadros nominal é designada como 1000. (Uma taxa de 500 é metade da velocidade normal, 2000 é duas vezes A velocidade normal e assim por diante.) Definir a velocidade como zero reproduz o vídeo o mais rápido possível sem descartar quadros e sem áudio.</td>
</tr>
<tr class="odd">
<td><em>formato</em> de formato de arquivo ainda</td>
<td>Especifica o formato de arquivo usado para comandos de captura.</td>
</tr>
<tr class="even">
<td>tempo tempo_value</td>
<td>Define o tempo da sequência de acordo com o formato de hora atual. Para um arquivo baseado em PPQN, o tempo_value é interpretado como batidas por minuto. Para um arquivo baseado em SMPTE, o tempo_value é interpretado como quadros por segundo.</td>
</tr>
<tr class="odd">
<td>bytes de formato de hora</td>
<td>Em um formato de arquivo PCM, define o formato de hora como bytes. Todas as informações de posição são especificadas como bytes após este comando.</td>
</tr>
<tr class="even">
<td>quadros de formato de hora</td>
<td>Define o formato de hora como quadros. Todos os comandos que usam valores de posição assumirão quadros. Quando o dispositivo é aberto, quadros é o modo padrão. Com suporte pelo videodiscs usando o formato CAV.</td>
</tr>
<tr class="odd">
<td>HMS de formato de hora</td>
<td>Define o formato de hora para horas, minutos e segundos. Todos os comandos que usam valores de posição assumirão HMS. HMS é o formato padrão para CLV videodiscs. Especifique um valor de HMS como hh: mm: SS, em que HH é horas, mm é minutos e SS é segundos. Você pode omitir um campo se ele e todos os campos a seguir forem zero. Por exemplo, 3, 3:0 e 3:0:0 são maneiras válidas de expressar 3 horas. <br/></td>
</tr>
<tr class="even">
<td>milissegundos de formato de hora</td>
<td>Define o formato de hora como milissegundos. Todos os comandos que usam valores de posição pressupõem milissegundos. Você pode abreviar milissegundos como &quot; MS &quot; . Para dispositivos do Sequencer, o arquivo de sequência define o formato padrão como PPQN ou SMPTE. Os dispositivos de sobreposição de vídeo não dão suporte a esse sinalizador.<br/></td>
</tr>
<tr class="odd">
<td>meio do formato de hora MSF</td>
<td>Define o formato de hora como minutos, segundos e quadros. Todos os comandos que usam valores de posição assumirão o MSF (o formato padrão para áudio de CD). Especifique um valor do MSF como mm: SS: FF, em que mm é minutos, SS é segundos e FF são quadros. Você pode omitir um campo se ele e todos os campos a seguir forem zero. Por exemplo, 3, 3:0 e 3:0:0 são maneiras válidas de expressar 3 minutos.<br/> Os campos do MSF têm os seguintes valores máximos:<br/>
<ul>
<li>Minutos 99</li>
<li>Segundos de 59</li>
<li>Quadros 74</li>
</ul></td>
</tr>
<tr class="even">
<td>exemplos de formato de hora</td>
<td>Define o formato de hora como exemplos. Todas as informações de posição são especificadas como exemplos após este comando.</td>
</tr>
<tr class="odd">
<td>formato de hora SMPTE 24<br/> formato de hora SMPTE 25<br/> formato de hora SMPTE 30<br/></td>
<td>Define o formato de hora como uma taxa de quadros SMPTE. Para VCRs, define o formato de hora como hh: mm: SS: FF, em que os valores válidos são de 00:00:00:00 a 23:59:59: XX e XX é um valor menor do que os quadros por segundo, conforme especificado pelo número 24, 25 ou 30, conforme especificado no sinalizador. Na entrada, dois-pontos (:) são necessários para separar os componentes. As unidades menos significativas podem ser omitidas se forem 00; por exemplo, 02:00 é o mesmo que 02:00:00:00. Todos os comandos que usam valores de posição assumirão o formato SMPTE.<br/> O arquivo de sequência define o formato padrão como PPQN ou SMPTE.<br/></td>
</tr>
<tr class="even">
<td>drop de formato de hora SMPTE 30</td>
<td>Define o formato de hora para a taxa de descarte de quadros SMPTE 30. Para VCRs, igual a SMPTE 30, exceto que determinadas posições de código de tempo são removidas do formato para que as posições de código de tempo registradas para cada quadro (na taxa de quadros NTSC de 29,97 fps) correspondam a tempo real (a 30 fps). As posições de código de tempo que são descartadas são as seguintes: duas a cada minuto, no minuto, para os nove primeiros de cada dez minutos de conteúdo registrado. Por exemplo, às 01:04:59:29, a próxima posição do código de tempo seria 01:05:00:02, e não 01:05:00:00. Todos os comandos que usam valores de posição assumirão o formato SMPTE.<br/> O arquivo de sequência define o formato padrão como PPQN ou SMPTE.<br/></td>
</tr>
<tr class="odd">
<td>ponteiro de música de formato de hora</td>
<td>Define o formato de hora para o ponteiro de música (dezesseis observações). Todos os comandos que usam valores de posição assumirão unidades de ponteiro de música. Esse sinalizador só é válido para uma sequência de tipo de divisão PPQN.</td>
</tr>
<tr class="even">
<td>tmsf de formato de hora</td>
<td>Define o formato de hora para faixas, minutos, segundos e quadros. Todos os comandos que usam valores de posição assumirão TMSF. Especifique um valor de TMSF como TT: mm: SS: FF, em que TT é faixas, mm é minutos, SS é segundos e FF é quadros. Você pode omitir um campo se ele e todos os campos a seguir forem zero. Por exemplo, 3, 3:0, 3:0:0 e 3:0:0:0 são maneiras válidas de expressar o Track 3. <br/> Os campos TMSF têm os seguintes valores máximos:<br/>
<ul>
<li>Faixas 99</li>
<li>Minutos 90</li>
<li>Segundos de 59</li>
<li>Quadros 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>faixa de formato de hora</td>
<td>Define o formato de posição como faixas. Todos os comandos que usam valores de posição assumirão faixas.</td>
</tr>
<tr class="even">
<td>contador de modo de tempo</td>
<td>Define o modo de informações de posição para usar os contadores de VCR.</td>
</tr>
<tr class="odd">
<td>detecção de modo de tempo</td>
<td>Define o modo de informações de posição com base na detecção de informações de código de Code na fita. Se as informações de código de tempo forem detectadas, o tipo de hora será definido como código de tempo &quot; &quot; ; caso contrário, o tipo de hora será definido como &quot; contador &quot; . &quot;Detectar &quot; é um modo especial. Sempre que o driver é aberto, uma nova fita é inserida ou o &quot; comando de modo de tempo &quot; é emitido, o driver verifica o modo de tempo atual disponível na fita e define o &quot; tipo &quot; de hora como um código de tempo &quot; &quot; ou &quot; contador &quot; . Quando &quot; o tipo &quot; de hora é definido, o driver não o altera até que uma das condições acima ocorra novamente.<br/></td>
</tr>
<tr class="even">
<td>tempo de vida de modo de hora</td>
<td>Define o modo de informações de posição para usar &quot; informações de código &quot; de Code na fita.</td>
</tr>
<tr class="odd">
<td>acompanhamento de mais <br/> menos controle <br/> redefinição de rastreamento <br/></td>
<td>Ajusta a velocidade do transporte de fita em incrementos finos. Use os &quot; sinalizadores de rastreamento &quot; quando uma imagem ruidosa for Obtida de um videocassete. &quot;O acompanhamento &quot; do Plus aumenta a velocidade de transporte. &quot;O rastreamento &quot; de menos diminui a velocidade de transporte. &quot;A redefinição &quot; de controle retorna o ajuste de controle para zero.</td>
</tr>
<tr class="even">
<td>vídeo desativado</td>
<td>Desabilita a saída de vídeo.</td>
</tr>
<tr class="odd">
<td>vídeo ativado</td>
<td>Habilita a saída de vídeo.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Várias propriedades dos dados de formato de onda-áudio são definidas quando o arquivo para armazenar os dados é criado. Essas propriedades descrevem como os dados são estruturados dentro do arquivo e não podem ser alterados após o início da gravação. A lista a seguir identifica essas propriedades:

-   alinhamento
-   bitspersample
-   bytespersec
-   canais
-   marca de formato
-   samplespersec

## <a name="examples"></a>Exemplos

O comando a seguir define o formato de hora como milissegundos e define o formato de wave-áudio para 8 bits, mono, 11 kHz.

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

[captura](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[salvar](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

