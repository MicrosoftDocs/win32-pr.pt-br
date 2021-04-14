---
title: comando de busca
description: O comando Seek move para a posição especificada e para. CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- Multimídia do Windows de comando de busca
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369249"
---
# <a name="seek-command"></a>comando de busca

O comando Seek move para a posição especificada e para. CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*
</dt> <dd>

Sinalizador para mover para uma posição especificada. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **busca** e os sinalizadores usados por cada tipo.



| Valor        | Significado                          | Significado                      |
|--------------|----------------------------------|------------------------------|
| cdaudio      | até a *posição* final             | para iniciar                     |
| digitalvideo | até a *posição* final             | para iniciar                     |
| sequenciador    | até a *posição* final             | para iniciar                     |
| videocassete          | em *\_ número* de marca de *tempo* invertido | até a *posição* final para iniciar |
| videodisc    | reverter para fim                   | para *posição* para iniciar        |
| waveaudio    | até a *posição* final             | para iniciar                     |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszSeekFlags** e seus significados.



| Valor            | Significado                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| às *vezes*        | Indica quando o dispositivo deve começar a executar este comando ou, se o dispositivo tiver sido cued, quando o comando cued for iniciado. Para obter mais informações, consulte o comando [Cue](cue.md) .                             |
| marcar *\_ número* de marca | Busca a marca relativa indicada por *Mark \_ num*, que deve ser um valor inteiro positivo. Marcas são sinais gravados na fita VCR usando o comando [Mark](mark.md) e são usados para pesquisa de alta velocidade. |
| reverse          | Indica que a direção de busca em VCRs e CAV videodiscs é retroativa. Esse sinalizador é inválido se o sinalizador "to" for especificado. Para VCRs, esse sinalizador deve ser usado com o sinalizador "Mark".                             |
| para o fim           | Busca o fim do conteúdo.                                                                                                                                                                                 |
| para a *posição*    | Especifica a posição para parar a busca. Para dispositivos **cdaudio** , o MCI retornará um erro fora do intervalo se a posição especificada for maior do que o comprimento do disco.                                            |
| para iniciar         | Busca o início do conteúdo.                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .

Os dispositivos de vídeo digital dão suporte a dois modos de busca, que podem ser alterados usando o comando [set](set.md) . O modo "Seek exactly on" faz com que o comando Seek seja movido para o quadro especificado. O modo "Seek exactly off" faz com que o comando Seek se mova para o quadro-chave mais próximo antes do quadro especificado.

Se um dispositivo de áudio de CD estiver sendo executado quando o comando de busca for emitido, a reprodução será interrompida. Quando o comando Seek é emitido com um dispositivo VIDEODISC, o dispositivo pesquisa usando Fast forward ou Fast reverso com vídeo e áudio desligados.

Quando o comando Seek é emitido com um dispositivo wave-Audio, o comportamento depende do tamanho da amostra. Se o tamanho da amostra for de 16 bits ou maior, o Seek passará para o início do exemplo mais próximo quando uma posição especificada não coincidir com o início de um exemplo.

## <a name="examples"></a>Exemplos

O comando a seguir procura o início do arquivo de mídia associado ao dispositivo "mysound".

``` syntax
seek mysound to start
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

[advertência](cue.md)
</dt> <dt>

[marca](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

