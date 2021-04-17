---
title: comando Play
description: O comando Play começa a reproduzir um dispositivo. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- reproduzir multimídia do Windows do comando
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758747"
---
# <a name="play-command"></a>comando Play

O comando Play começa a reproduzir um dispositivo. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Sinalizador para reproduzir um dispositivo. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Play** e os sinalizadores usados por cada tipo.



| Valor        | Significado                          | Significado                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | da *posição*                  | para a *posição*                     |
| digitalvideo | da *posição* de tela inteira repetir | reverter para a janela de *posição*       |
| sequenciador    | da *posição*                  | para a *posição*                     |
| videocassete          | às *vezes* a partir da *posição* inversa  | Digitalizar para *posição*                |
| videodisc    | rápida da verificação reversa de *posição* | menor velocidade do *inteiro* para *posição* |
| waveaudio    | da *posição*                  | para a *posição*                     |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszPlayFlags** e seus significados.



| Valor           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| às *vezes*       | Indica quando o dispositivo deve começar a executar este comando ou, se o dispositivo tiver sido cued, quando o comando cued for iniciado. Para obter mais informações, consulte o comando [Cue](cue.md) .                                                                                                                                                                                                                                                                 |
| rápido            | Indica que o dispositivo deve ser executado mais rápido do que o normal. Para determinar a velocidade exata em um VIDEODISC Player, use o sinalizador "velocidade" do comando de [status](status.md) . Para especificar a velocidade mais precisamente, use o sinalizador "velocidade" desse comando.                                                                                                                                                                                                   |
| da *posição* | Especifica uma posição inicial para a reprodução. Se o sinalizador "from" não for especificado, a reprodução começará na posição atual. Para dispositivos **cdaudio** , se a posição "de" for maior que a posição final do disco, ou se a posição "de" for maior que a posição "para", o driver retornará um erro. Para dispositivos **VIDEODISC** , as posições padrão estão em quadros para discos CAV e em horas, minutos e segundos para discos CLV. |
| tela inteira      | Especifica que uma exibição de tela inteira deve ser usada. Use este sinalizador somente ao reproduzir arquivos compactados. (Arquivos não compactados não serão exibidos em tela inteira.)                                                                                                                                                                                                                                                                                                  |
| Pete          | Especifica que a reprodução deve ser reiniciada quando o final do conteúdo é atingido.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Especifica que a direção da execução é retroativa. Não é possível especificar um local final com o sinalizador "Reverse". Para videodiscs, "Scan" aplica-se somente ao formato CAV.                                                                                                                                                                                                                                                                                     |
| scanner            | É reproduzido o mais rápido possível sem desabilitar o vídeo (embora o áudio possa estar desabilitado). Para videodiscs, "Scan" aplica-se somente ao formato CAV.                                                                                                                                                                                                                                                                                                             |
| lento            | É reproduzido lentamente. Para determinar a velocidade exata em um VIDEODISC Player, use o sinalizador "velocidade" do comando de [status](status.md) . Para especificar a velocidade mais precisamente, use o sinalizador "velocidade" desse comando. Para videodiscs, "lento" aplica-se somente ao formato CAV.                                                                                                                                                                                            |
| *número inteiro* de velocidade | Reproduz um VIDEODISC na velocidade especificada, em quadros por segundo. Esse sinalizador se aplica somente a discos CAV.                                                                                                                                                                                                                                                                                                                                                 |
| para a *posição*   | Especifica uma posição final para a reprodução. Se o sinalizador "to" não for especificado, a reprodução será interrompida no final do conteúdo. Para dispositivos **cdaudio** , se a posição "para" for maior que a posição final do disco, o driver retornará um erro. Para dispositivos **VIDEODISC** , as posições padrão estão em quadros para discos CAV e em horas, minutos e segundos para discos CLV.                                                                  |
| janela          | Especifica que a execução deve usar a janela associada à instância do dispositivo. Essa é a configuração padrão.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) . Esse comando começa a reproduzir na velocidade atual, conforme definido com o comando Set "Speed". A direção será inversa se o sinalizador "Reverse" for especificado ou se o sinalizador "to" for especificado como um valor menor do que o sinalizador "from". Se o sinalizador "from" não for especificado, a reprodução começará na posição atual. Os sinalizadores "para" e "reverso" não podem ser usados juntos.

## <a name="examples"></a>Exemplos

O comando a seguir reproduz o dispositivo "mysound" da posição 1000 até a posição 2000, enviando uma mensagem de notificação quando a reprodução é concluída.

``` syntax
play mysound from 1000 to 2000 notify
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

[set](set.md)
</dt> </dl>

 

