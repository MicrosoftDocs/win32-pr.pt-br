---
title: comando open (Corecrt \_ io.h)
description: O comando open inicializa um dispositivo. Todos os dispositivos MCI reconhecem esse comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- abrir comando Windows Multimídia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d2e585a44c19093fa0d20ab4870f579c67cd568c3a693523242b84910e6589d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373265"
---
# <a name="open-command"></a>comando open

O comando open inicializa um dispositivo. Todos os dispositivos MCI reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*
</dt> <dd>

Identificador de um driver de dispositivo ou dispositivo MCI. Isso pode ser um nome de dispositivo (conforme determinado no Registro ou no arquivo SYSTEM.INI) ou o nome de arquivo do driver de dispositivo. Se você especificar o nome do arquivo do driver de dispositivo, opcionalmente, poderá incluir o . Extensão DRV, mas você não deve incluir o caminho para o arquivo.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Sinalizador que identifica o que inicializar. A tabela a seguir lista os tipos de dispositivo que reconhecem o **comando open** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                        | Significado                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias de *\_ alias de dispositivo* compartilhável                                  | tipo *\_ de dispositivo*                                                             |
| digitalvideo | alias *alias \_ device aliaselementname* nostatic parent *hwnd* compartilhável | style child style overlapped style popup style *type \_* device *\_ type* |
| overlay      | alias *do alias do \_ dispositivo* pai *hwnd* filho de estilo compartilhável         | style overlapped style pop-up *style style \_ type* *device \_ type*             |
| sequenciador    | alias de *\_ alias de dispositivo* compartilhável                                 | tipo *\_ de dispositivo*                                                             |
| Videocassete          | alias de *\_ alias de dispositivo* compartilhável                                  | tipo *\_ de dispositivo*                                                             |
| videodisk    | alias de *\_ alias de dispositivo* compartilhável                                  | tipo *\_ de dispositivo*                                                             |
| Waveaudio    | tamanho do buffer *\_ de buffer do alias* do dispositivo *de \_* alias                     | tipo de dispositivo *\_ compartilhável*                                                    |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no **parâmetro lpszOpenFlags** e seus significados.



| Valor                 | Significado                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alias *do dispositivo de \_ alias* | Especifica um nome alternativo para o dispositivo especificado. Se especificado, ele deve ser usado como a *\_ ID do dispositivo nos* comandos subsequentes.                                                                                                                                                                                                                                          |
| *Elementname*         | Especifica o nome do elemento do dispositivo (arquivo) carregado quando o dispositivo é aberto.                                                                                                                                                                                                                                                                                        |
| tamanho *do buffer de \_ buffer* | Define o tamanho, em segundos, do buffer usado pelo dispositivo waveform-audio. O tamanho padrão do buffer é definido quando o dispositivo waveform-audio é instalado ou configurado. Normalmente, o tamanho do buffer é definido como 4 segundos. Com o dispositivo MCIWAVE, o tamanho mínimo é de 2 segundos e o tamanho máximo é de 9 segundos.                                                |
| pai *hwnd*         | Especifica o alça de janela da janela pai.                                                                                                                                                                                                                                                                                                                    |
| Compartilhável              | Inicializa o dispositivo ou arquivo como compartilhável. As tentativas subsequentes de abrir o dispositivo ou o arquivo falharão, a menos que você especifique "compartilhável" nos comandos abertos originais **e subsequentes.** A MCI retornará um erro de dispositivo inválido se o dispositivo já estiver aberto e não for compartilhável.<br/> Os dispositivos mciseq sequencer e MCIWAVE não são compatíveis com arquivos compartilhados.<br/> |
| style child           | Abre uma janela com um estilo de janela filho.                                                                                                                                                                                                                                                                                                                            |
| estilo sobre-mapeado      | Abre uma janela com um estilo de janela sobressalo.                                                                                                                                                                                                                                                                                                                      |
| pop-up de estilo           | Abre uma janela com um estilo de janela pop-up.                                                                                                                                                                                                                                                                                                                           |
| tipo *\_ de estilo*   | Indica um estilo de janela.                                                                                                                                                                                                                                                                                                                                            |
| tipo *\_ de dispositivo*   | Especifica o tipo de dispositivo de um arquivo.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

A MCI reserva "cdaudio" para o tipo de dispositivo de áudio CD, "videodisc" para o tipo de dispositivo videodisc, "sequencer" para o tipo de dispositivo MIDI sequencer, "AVIVideo" para o tipo de dispositivo de vídeo digital e "waveaudio" para o tipo de dispositivo waveform-audio.

Como alternativa ao sinalizador "type", a MCI pode selecionar o dispositivo com base na extensão usada pelo arquivo, conforme registrado no Registro ou na seção de extensão mci do arquivo \[ \] SYSTEM.INI.

A MCI pode abrir arquivos AVI usando um ponteiro de interface de arquivo ou um ponteiro de interface de fluxo. Para abrir um arquivo usando qualquer tipo de ponteiro de interface, especifique um sinal de ata (@) seguido pelo ponteiro de interface no lugar do nome do arquivo ou do dispositivo para o *parâmetro lpszDevice.* Para obter mais informações sobre as interfaces de arquivo e fluxo, consulte " [Funções e macros AVIFile](avifile-functions-and-macros.md)".

O comando a seguir abre o dispositivo "mysound".

``` syntax
open new type waveaudio alias mysound buffer 6
```

Com o nome do dispositivo "novo", o driver waveform prepara um novo recurso de forma de onda. O comando atribui o alias do dispositivo "mysound" e especifica um buffer de 6 segundos.

Você poderá eliminar o sinalizador "tipo" se combinar o nome do dispositivo com o nome do arquivo. A MCI reconhece essa combinação quando você usa a seguinte sintaxe:

*nome \_ do dispositivo* ! *nome do \_ elemento*

O ponto de exclamação separa o nome do dispositivo do nome do arquivo. O ponto de exclamação não deve ser delimitado por espaços em branco.

O exemplo a seguir abre RIGHT. Arquivo WAV usando o dispositivo "waveaudio".

``` syntax
open waveaudio!right.wav
```

O driver MCIWAVE requer um dispositivo assíncrono waveform-audio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

