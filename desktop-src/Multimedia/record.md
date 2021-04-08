---
title: comando gravar
description: O comando gravar começa a gravar dados. Os dispositivos VCR e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- gravar comando multimídia do Windows
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824182"
---
# <a name="record-command"></a>comando gravar

O comando gravar começa a gravar dados. Os dispositivos VCR e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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

Sinalizador para gravar dados. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **registro** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                | Significado                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | *fluxo* de fluxo de áudio no *retângulo* da espera de *posição* | inserir substituição para *posicionar* *fluxo* de fluxo de vídeo |
| sequenciador    | da *posição* de inserção                                  | substituir na *posição*                             |
| videocassete          | no *momento* da inicialização da *posição*                     | inserir substituição na *posição*                      |
| waveaudio    | da *posição* de inserção                                  | substituir na *posição*                             |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRecordFlags** e seus significados.



| Valor                 | Significado                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo*        | Especifica uma região retangular da entrada externa usada como a origem dos pixels compactados e salvos. Se não for especificado, o retângulo usa como padrão o retângulo especificado para [colocar](put.md) "vídeo". Quando ele é definido de forma diferente do retângulo de "vídeo", a imagem exibida não é o que é registrado. |
| às *vezes*             | Indica quando o dispositivo deve começar a executar este comando ou, se o dispositivo tiver sido cued, quando o comando cued for iniciado. Para obter mais informações, consulte o comando [Cue](cue.md) .                                                                                                                             |
| *fluxo* de fluxo de áudio | Especifica o fluxo de áudio usado para gravação. Se esse sinalizador não for especificado e o formato de arquivo não definir um padrão, ele será gravado no fluxo que é fisicamente primeiro.                                                                                                                             |
| da *posição*       | Especifica uma posição inicial para a gravação. Se o sinalizador "from" não for especificado, o dispositivo começará a gravar na posição atual.                                                                                                                                                                       |
| bloqueio                  | Congela a imagem quando a gravação termina em vez de mostrar o vídeo ao vivo. Quando a gravação é interrompida, um comando "arquivo" de [Monitor](monitor.md) automático é executado. Para retornar ao vídeo ao vivo, emita o comando "Input" do **Monitor** .                                                                              |
| inicializar            | Inicialize a fita (mídia), que envolve a gravação de código de paficação (se possível) para vídeo e áudio em branco. Esse comando poderá levar várias horas se a fita inteira precisar ser inicializada.                                                                                                                            |
| insert                | Especifica que novos dados são adicionados ao arquivo na posição atual.                                                                                                                                                                                                                                            |
| overwrite             | Especifica que novos dados substituirão os dados no arquivo.                                                                                                                                                                                                                                                           |
| para a *posição*         | Especifica uma posição final para a gravação. Se o sinalizador "to" não for especificado, o dispositivo será registros até receber um comando [Stop](stop.md) ou [Pause](pause.md) .                                                                                                                                        |
| *fluxo* de fluxo de vídeo | Especifica o fluxo de vídeo usado para gravação. Se isso não for especificado e o formato de arquivo não definir um padrão, ele será gravado no fluxo que é fisicamente primeiro.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A gravação é interrompida quando um comando [Stop](stop.md) ou [Pause](pause.md) é emitido. Para o driver MCIWAVE, todos os dados gravados após a abertura de um arquivo serão descartados se o arquivo for fechado sem salvá-lo.

Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) . As faixas a serem registradas são especificadas pelo comando [SetCode](settimecode.md) "Record", defina os comandos "montar registro", [setvideo](setvideo.md) "registro" e "registro" de conjunto de [áudio](setaudio.md) .

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

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[advertência](cue.md)
</dt> <dt>

[monitor](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Posicione](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[SetCode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

