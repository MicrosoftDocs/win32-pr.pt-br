---
title: Comando record
description: O comando record inicia a gravação de dados. Os dispositivos VCR e waveform-audio reconhecem esse comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- comando record Windows Multimídia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f326b13d86f073074ef2c1119d449e297e65e7d3accb22d9858e5c1579493c01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037556"
---
# <a name="record-command"></a>Comando record

O comando record inicia a gravação de dados. Os dispositivos VCR e waveform-audio reconhecem esse comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

Sinalizador para gravação de dados. A tabela a seguir lista os tipos de dispositivo que reconhecem **o comando de** registro e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                | Significado                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | no *fluxo de* fluxo de áudio do *retângulo* da *posição* | inserir substituir para posicionar o *fluxo* de fluxo de *vídeo* |
| sequenciador    | da *inserção de* posição                                  | substituir na *posição*                             |
| Videocassete          | no *momento* da *inicialização da* posição                     | inserir substituir na *posição*                      |
| Waveaudio    | da *inserção de* posição                                  | substituir na *posição*                             |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRecordFlags** e seus significados.



| Valor                 | Significado                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| retângulo *em*        | Especifica uma região retangular da entrada externa usada como a origem para os pixels compactados e salvos. Se não for especificado, o retângulo assume como padrão o retângulo especificado para [colocar](put.md) "vídeo". Quando ele é definido de forma diferente do retângulo "vídeo", a imagem exibida não é o que é gravado. |
| no *momento*             | Indica quando o dispositivo deve começar a executar esse comando ou, se o dispositivo foi cued, quando o comando cued começa. Para obter mais informações, consulte o [comando de indicação.](cue.md)                                                                                                                             |
| fluxo de fluxo de *áudio* | Especifica o fluxo de áudio usado para gravação. Se esse sinalizador não for especificado e o formato de arquivo não definir um padrão, ele será registrado no fluxo que é fisicamente primeiro.                                                                                                                             |
| da *posição*       | Especifica uma posição inicial para a gravação. Se o sinalizador "from" não for especificado, o dispositivo começará a gravar na posição atual.                                                                                                                                                                       |
| Segurar                  | Congela a imagem quando a gravação é concluída, em vez de mostrar um vídeo ao vivo. Quando a gravação é interrompida, um [comando](monitor.md) "arquivo" do monitor automático é executado. Para retornar ao vídeo ao vivo, emito **o comando** "entrada" do monitor.                                                                              |
| Inicializar            | Inicialize a fita (mídia), que envolve a gravação de código de data/hora (se possível) para vídeo e áudio em branco. Esse comando poderá levar várias horas se toda a fita precisar ser inicializada.                                                                                                                            |
| insert                | Especifica que novos dados são adicionados ao arquivo na posição atual.                                                                                                                                                                                                                                            |
| overwrite             | Especifica que novos dados substituirão os dados no arquivo.                                                                                                                                                                                                                                                           |
| para *posicionar*         | Especifica uma posição final para a gravação. Se o sinalizador "to" não for especificado, o dispositivo registra até receber um comando [parar](stop.md) ou [pausar.](pause.md)                                                                                                                                        |
| fluxo de fluxo de *vídeo* | Especifica o fluxo de vídeo usado para gravação. Se isso não for especificado e o formato de arquivo não definir um padrão, ele será registrado no fluxo que é fisicamente primeiro.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

A gravação é interrompida quando [um comando parar](stop.md) [ou](pause.md) pausar é emitido. Para o driver MCIWAVE, todos os dados registrados após a abertura de um arquivo serão descartados se o arquivo for fechado sem salvá-lo.

Antes de emissão de comandos que usam valores de posição, você deve definir o formato de hora desejado usando o [comando set.](set.md) As faixas a serem registradas são especificadas pelos comandos [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record" e [setaudio](setaudio.md) "record".

## <a name="examples"></a>Exemplos

O comando a seguir inicia a gravação na posição atual.

``` syntax
record mysound
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[Cue](cue.md)
</dt> <dt>

[Monitor](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Colocar](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[Setaudio](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

