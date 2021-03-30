---
title: comando abrir (Corecrt \_ Io. h)
description: O comando abrir Inicializa um dispositivo. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- abrir o comando multimídia do Windows
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
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644632"
---
# <a name="open-command"></a>Abrir comando

O comando abrir Inicializa um dispositivo. Todos os dispositivos MCI reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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

Identificador de um dispositivo MCI ou driver de dispositivo. Pode ser um nome de dispositivo (conforme fornecido no registro ou no arquivo de SYSTEM.INI) ou o nome de arquivo do driver de dispositivo. Se você especificar o nome de arquivo do driver de dispositivo, você pode opcionalmente incluir o. Extensão DRV, mas você não deve incluir o caminho para o arquivo.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Sinalizador que identifica o que inicializar. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Open** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                        | Significado                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | *\_ alias de dispositivo* de alias compartilhável                                  | Digite *o \_ tipo de dispositivo*                                                             |
| digitalvideo | dispositivo de alias *\_ aliaselementname* não static pai *hWnd* compartilhável | tipo de *estilo \_* de estilo filho estilo sobreposto Style tipo de *dispositivo \_* tipo |
| overlay      | alias *de \_ dispositivo* de alias pai *hWnd* de estilo compartilhável filho         | estilo de estilo sobreposto estilo *de \_ tipo de estilo* não tipo tipo de *dispositivo \_*             |
| sequenciador    | *\_ alias de dispositivo* de alias compartilhável                                 | Digite *o \_ tipo de dispositivo*                                                             |
| videocassete          | *\_ alias de dispositivo* de alias compartilhável                                  | Digite *o \_ tipo de dispositivo*                                                             |
| videodisk    | *\_ alias de dispositivo* de alias compartilhável                                  | Digite *o \_ tipo de dispositivo*                                                             |
| waveaudio    | *\_ tamanho do buffer* de buffer do *\_ alias de dispositivo* de alias                     | tipo de *dispositivo \_* compartilhável                                                    |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszOpenFlags** e seus significados.



| Valor                 | Significado                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *\_ alias de dispositivo* de alias | Especifica um nome alternativo para o dispositivo especificado. Se especificado, ele deve ser usado como a *\_ ID do dispositivo* em comandos subsequentes.                                                                                                                                                                                                                                          |
| *ElementName*         | Especifica o nome do elemento do dispositivo (arquivo) carregado quando o dispositivo é aberto.                                                                                                                                                                                                                                                                                        |
| *\_ tamanho do buffer* de buffer | Define o tamanho, em segundos, do buffer usado pelo dispositivo de formato de onda-áudio. O tamanho padrão do buffer é definido quando o dispositivo de formato de onda-áudio é instalado ou configurado. Normalmente, o tamanho do buffer é definido como 4 segundos. Com o dispositivo MCIWAVE, o tamanho mínimo é de 2 segundos e o tamanho máximo é de 9 segundos.                                                |
| *HWND* pai         | Especifica o identificador de janela da janela pai.                                                                                                                                                                                                                                                                                                                    |
| compartilháveis              | Inicializa o dispositivo ou o arquivo como compartilhável. As tentativas subsequentes de abrir o dispositivo ou arquivo falham, a menos que você especifique "compartilhável" nos comandos **abertos** original e subseqüente. O MCI retornará um erro de dispositivo inválido se o dispositivo já estiver aberto e não puder ser compartilhado.<br/> Os dispositivos MCISEQ Sequencer e MCIWAVE não dão suporte a arquivos compartilhados.<br/> |
| filho do estilo           | Abre uma janela com um estilo de janela filho.                                                                                                                                                                                                                                                                                                                            |
| estilo sobreposto      | Abre uma janela com um estilo de janela sobreposto.                                                                                                                                                                                                                                                                                                                      |
| pop-up de estilo           | Abre uma janela com um estilo de janela pop-up.                                                                                                                                                                                                                                                                                                                           |
| *\_ tipo de estilo* de estilo   | Indica um estilo de janela.                                                                                                                                                                                                                                                                                                                                            |
| Digite *o \_ tipo de dispositivo*   | Especifica o tipo de dispositivo de um arquivo.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O MCI reserva "cdaudio" para o tipo de dispositivo de áudio de CD, "VIDEODISC" para o tipo de dispositivo VIDEODISC, "Sequencer" para o tipo de dispositivo Sequencer MIDI, "AVIVideo" para o tipo de dispositivo digital-video e "WaveAudio" para o tipo de dispositivo wave de onda-áudio.

Como uma alternativa ao sinalizador "tipo", o MCI pode selecionar o dispositivo com base na extensão usada pelo arquivo, conforme registrado no registro ou na \[ seção extensão MCI \] do arquivo de SYSTEM.INI.

O MCI pode abrir arquivos AVI usando um ponteiro de interface de arquivo ou um ponteiro de interface de fluxo. Para abrir um arquivo usando qualquer tipo de ponteiro de interface, especifique um sinal de arroba (@) seguido pelo ponteiro de interface no lugar do nome do arquivo ou do dispositivo para o parâmetro *lpszDevice* . Para obter mais informações sobre as interfaces de arquivo e fluxo, consulte " [funções e macros do avifile](avifile-functions-and-macros.md)".

O comando a seguir abre o dispositivo "mysound".

``` syntax
open new type waveaudio alias mysound buffer 6
```

Com o nome do dispositivo "novo", o driver de formato de onda prepara um novo recurso de formato de onda. O comando atribui o alias de dispositivo "mysound" e especifica um buffer de 6 segundos.

Você pode eliminar o sinalizador "tipo" se combinar o nome do dispositivo com o nome do arquivo. O MCI reconhece essa combinação quando você usa a seguinte sintaxe:

*\_ nome do dispositivo* ! *nome do elemento \_*

O ponto de exclamação separa o nome do dispositivo do nome de arquivo. O ponto de exclamação não deve ser delimitado por espaços em branco.

O exemplo a seguir abre a direita. Arquivo WAV usando o dispositivo "WaveAudio".

``` syntax
open waveaudio!right.wav
```

O driver MCIWAVE requer um dispositivo de áudio de onda assíncrono.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Corecrt \_ Io. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

