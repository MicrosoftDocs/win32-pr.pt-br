---
title: comando setvideo
description: O comando setvideo define os valores associados à captura e reprodução de vídeo. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- Multimídia do Windows de comando do setvideo
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa4c3d1e3b90b9ab0c5bf5791dacd541c8a8bc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369707"
---
# <a name="setvideo-command"></a>comando setvideo

O comando setvideo define os valores associados à captura e reprodução de vídeo. Os dispositivos de vídeo digital e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("setvideo %s %s %s"), 
  lpszDeviceID, 
  lpszVideo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszVideo*
</dt> <dd>

Sinalizador para reprodução e captura de vídeo. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **setvideo** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | *algoritmo* de algoritmo BitsPerPel para *contar* o brilho para *fator* clocktimecolor para *fatorar* contraste com o *fator* gama ao *valor* de halftoneinputkey cor para *r:g: b* índice de chave para *índice* offonoutput | a *cor* de cor da paleta de *duração* acima do *índice* para o identificador da paleta do *newrgb* para *lidar* com a taxa de quadros de registro do *descritor* *de qualidade para* *classificar* o *valor* do registro de offsharpness para a origem do *fator* *para o número de* *origem* ainda *algoritmo* *de* algoritmos de fluxo |
| videocassete          | offonmonitor para *digitar* número *de número de registro offrecord* faixa *de controle de faixas \_*                                                                                                               | registrar *\_ número de faixa* de controle de *registro por fonte \_* para o *tipo* *número numérico faixa faixas* *número \_ de faixa offtrack*                                                                                                                                                                             |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszVideo** e seus significados.



| Valor                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algoritmo* de algoritmo                          | Especifica um algoritmo de compactação de vídeo para uso por um comando de [reserva](reserve.md) ou de [registro](record.md) subsequente. Os algoritmos com suporte de um dispositivo são específicos ao dispositivo. O MCI define as constantes "MPEG" e "H261" para o *algoritmo*. Se o algoritmo especificado estiver em conflito com o formato de arquivo atual, o formato de arquivo será alterado para o formato padrão do algoritmo.<br/>                                                                                                                                     |
| BitsPerPel para *contagem*                          | Define o número de bits por pixel para salvar dados com o comando [Capture](capture.md) ou [Record](record.md) .                                                                                                                                                                                                                                                                                                                                                                                                              |
| brilho para *fator*                         | Define o nível de brilho do vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| horário de clock                                      | Indica que o tempo especificado no sinalizador "over" está em milissegundos. A hora é absoluta e não está em etapas com a reprodução do espaço de trabalho.                                                                                                                                                                                                                                                                                                                                                                                |
| cor a *fator*                              | Define o nível de saturação de cor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| contraste com o *fator*                           | Define o nível de contraste de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| gama para *valor*                               | Especifica o expoente de correção gama multiplicado por 1000. Por exemplo, para especificar um expoente de 2,2, use 2200 para *valor*. Um valor de gama de 1,0 (1000) indica que nenhuma correção de gama foi aplicada. A correção gama ajusta o mapeamento entre a intensidade codificada na fonte da apresentação e o brilho exibido.                                                                                                                                                                                                 |
| proje                                       | Faz com que a paleta de meio-tom seja usada em vez da paleta padrão. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Modifica o sinalizador "brilho", "cor", "contraste", "gama", "nitidez" ou "tonalidade" para que ele afete o sinal de entrada e modifique o que é registrado. Se possível, esse é o padrão ao monitorar a entrada.                                                                                                                                                                                                                                                                                                             |
| cor da chave para *r:g: b*                           | Define a cor da chave. A variável *r:g: b* é um valor RGB. Dois-pontos (:) Separe os valores individuais de vermelho, verde e azul.                                                                                                                                                                                                                                                                                                                                                                                                       |
| índice de chave para *índice*                           | Define o índice de chave. A variável de *índice* é um índice de paleta física.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| monitorar para *digitar* *número* numérico              | Controla qual entrada de origem será passada para a saída de VCR, sem alterar a seleção de entrada de fonte de gravação. O tipo pode ser "output" ou uma das fontes de entrada válidas. Se "Number" não for especificado, a primeira entrada desse tipo será escolhida.                                                                                                                                                                                                                                                                        |
| offon                                          | Habilita ou desabilita a exibição de vídeo. Desabilitar o vídeo define os pixels no retângulo "destino" [Put](put.md) (ou seu padrão, a região do cliente da janela atual) para uma cor sólida. Ele não tem nenhum efeito no buffer de quadros. A fonte de vídeo, seja o espaço de trabalho ou uma entrada externa, pode continuar armazenando novas imagens no buffer de quadros. Eles não serão exibidos até que o vídeo esteja habilitado. Você pode usar o comando "State" da [janela](window.md) para ocultar a janela. O padrão é **setvideo** "on".<br/> |
| output                                         | Modifica o sinalizador "brilho", "cor", "contraste", "gama", "nitidez" ou "tonalidade" para que ele modifique apenas o sinal exibido e não o que é registrado. Se possível, esse é o padrão ao monitorar um arquivo.                                                                                                                                                                                                                                                                                                           |
| acima da *duração*                                | Especifica quanto tempo deve levar para fazer uma alteração que usa uma variável de *fator* . As unidades de *duração* estão no formato de hora atual. As alterações ocorrem em etapa com a reprodução do espaço de trabalho. Quando a execução é suspensa, a alteração também é suspensa até que a reprodução continue. Se "over" não for usado ou não houver suporte, a alteração ocorrerá imediatamente.                                                                                                                                                                    |
| *cor* da cor da paleta sobre o *índice* para *newrgb* | Define uma nova cor de paleta. A cor e o índice da paleta a serem alterados são especificados pelos parâmetros de *cor* e *índice* ; a nova cor é especificada por *newrgb*. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.                                                                                                                                                                                                                                                                                               |
| identificador da paleta a ser *manipulado*                     | Especifica o identificador para uma paleta que o dispositivo deve usar para renderização. Esse item só tem suporte em dispositivos que usam paletas. Se o *identificador* for zero, a paleta padrão será usada. Os dispositivos de vídeo digital não devem liberar a paleta passada com esse comando. Os aplicativos devem liberá-lo depois que fecharem o dispositivo.<br/>                                                                                                                                                                                                 |
| *descritor* de qualidade                           | Especifica as características da compactação de vídeo executada quando o vídeo é gravado em um arquivo. Todos os dispositivos dão suporte aos três Descritores: "Low", "Medium" e "High". O padrão é específico do dispositivo. O significado desses nomes depende do algoritmo e do dispositivo. Os dispositivos podem definir nomes de descritores adicionais. O comando de [qualidade](quality.md) pode ser usado para definir nomes de descritores adicionais. Se o sinalizador "Algorithm" não for usado, o *descritor* se aplicará ao algoritmo atual.<br/>   |
| gravar a taxa de quadros para *classificar*                    | Define a gravação para o vídeo de movimento. A *taxa* de gravação é especificada em unidades de quadros por segundo multiplicada por 1000. Por exemplo, a taxa de quadros NTSC de 29,97 quadros por segundo é representada como 29970.                                                                                                                                                                                                                                                                                                                   |
| registro desgravado                            | Habilita ou desabilita a gravação de dados de vídeo. A gravação de dados de vídeo é o padrão.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| gravar *\_ número de faixas* de faixa               | Limpa a seleção de fonte de vídeo para que nenhum vídeo seja gravado com o próximo comando de [registro](record.md) . "Track" permite a seleção de faixa independente. Se "Track" não for especificado, será assumido um valor padrão de 1. Pode ser necessário primeiro emitir um comando [set](set.md) "montar registro off" antes que a gravação de vídeo possa ser desativada.                                                                                                                                                                     |
| gravar *\_ número de faixa* de faixa em                | Seleciona a fonte de vídeo a ser gravada com o próximo comando de **registro** . "Track" permite a seleção de faixa independente. Track 2 corresponde à faixa do PCM no Hi8. Se "Track" não for especificado, será assumido um padrão de 1.                                                                                                                                                                                                                                                                                                      |
| nitidez do *fator*                          | Define o nível de nitidez do vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *valor* de origem para o número de *origem*              | Define a origem da entrada de vídeo. Isso geralmente corresponde a conectores externos. As constantes definidas para *Source* incluem "RGB", "PAL", "NTSC", "SVIDEO" e "secam". Se houver mais de uma entrada do tipo especificado, o *valor* opcional "Number" indicará a entrada desejada. Por exemplo, **setvideo** "origem para o número NTSC 2" especifica a segunda entrada NTSC. Se a *origem* "para" for omitida, a origem absoluta será usada conforme definido pelo comando da [lista](list.md) "fonte de vídeo".<br/>            |
| *número* de número de origem para *tipo*               | Seleciona a fonte de vídeo a ser gravada na fita. O *tipo* deve ser "sintonizador", "line", "SVIDEO", "AUX", "Generic", "mudo" ou "RGB".                                                                                                                                                                                                                                                                                                                                                                                              |
| *algoritmo* de algoritmo ainda                    | Especifica o algoritmo de compactação de imagem ainda usado pelo comando de [captura](capture.md) . Cada dispositivo deve dar suporte a um *algoritmo* de "nenhum", o que significa que não há compactação. Esse é o padrão. Nesse caso, os dispositivos de vídeo digital salvam imagens ainda como bitmaps independentes de dispositivo RGB. Os dispositivos também podem oferecer suporte a uma lista específica do dispositivo de algoritmos adicionais.                                                                                                                                                           |
| *descritor* de qualidade ainda                     | Especifica as características da compactação de imagem ainda executada durante a captura de uma imagem ainda. Todos os dispositivos dão suporte aos descritores "Low", "Medium" e "High". O padrão é específico do dispositivo. Se o sinalizador "Algorithm" não for usado, o *descritor* se aplicará ao algoritmo atual.<br/> O comando de [qualidade](quality.md) pode ser usado para definir outros nomes de descritores.<br/>                                                                                                                            |
| fluxo para *número*                             | Especifica o fluxo de vídeo reproduzido do espaço de trabalho. Se o fluxo não for especificado e um fluxo padrão não for definido pelo formato de arquivo, o primeiro fluxo de vídeo intercalado fisicamente será reproduzido.                                                                                                                                                                                                                                                                                                                 |
| tonalidade a *fator*                               | Define a tonalidade da imagem. Normalmente, esse ajuste é modelado após o controle de tonalidade de muitos conjuntos de televisão de cor, com 250 significando verde, 750 significando vermelho e 0 (ou                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Para dispositivos VCR, usar setvideo com um sinalizador que desativa uma faixa individual (" *\_ número* de faixa de controle desativado") pode fazer com que seu aplicativo receba uma mensagem de status indicando que o comando não pôde ser executado. Alguns VCRs podem desativar apenas combinações de faixas, não faixas individuais; por exemplo, a primeira faixa de áudio e uma faixa de vídeo de um fita de vídeo. Nesse caso, basta usar [SetAudio](setaudio.md) e setvideo para continuar a desligar as outras faixas que compõem a combinação. O driver desligará as trilhas quando receber o comando para desativar a última faixa na combinação.

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

[list](list.md)
</dt> <dt>

[Posicione](put.md)
</dt> <dt>

[gravável](record.md)
</dt> <dt>

[reservado](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[Window](window.md)
</dt> </dl>

 

