---
title: Comando save
description: O comando save salva um arquivo MCI. Os dispositivos video-overlay e waveform-audio reconhecem esse comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não são compatíveis com ele.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Salvar comando Windows Multimídia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c7b4fb75f78f8468a204217f5a4fa1593a1c50d5db541a83070a7faed41cc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037476"
---
# <a name="save-command"></a>Comando save

O comando save salva um arquivo MCI. Os dispositivos video-overlay e waveform-audio reconhecem esse comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não são compatíveis com ele.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

Sinalizador que especifica o nome do arquivo que está sendo salvo e, opcionalmente, sinalizadores adicionais que modificam a operação de salvar. A tabela a seguir lista os tipos de dispositivo que reconhecem **o comando save** e os sinalizadores usados por cada tipo.



| Valor        | Significado              | Significado               |
|--------------|----------------------|-----------------------|
| digitalvideo | anular no *retângulo* | *filename* keepreserve |
| overlay      | retângulo *em*       | *Filename*            |
| sequenciador    | *Filename*           |                       |
| Waveaudio    | *Filename*           |                       |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no **parâmetro lpszFilename** e seus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Interrompe uma **operação de** salvar em andamento. Se usado, esse deve ser o único item presente.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| retângulo *em* | Especifica um retângulo relativo à origem do buffer de quadro. O *retângulo* é especificado como *X1 Y1 X2 Y2*. As coordenadas *X1 Y1 especificam* o canto superior esquerdo e as coordenadas *X2 Y2* especificam a largura e a altura. Para dispositivos de vídeo digital, o [comando de](capture.md) captura é usado para capturar o conteúdo do buffer de quadro.<br/>                                                                                                                                               |
| *Filename*     | Especifica o nome do arquivo a ser atribuído ao arquivo de dados. Se um caminho não for especificado, o arquivo será colocado no disco e no diretório especificado anteriormente no comando de reserva explícita [ou implícita.](reserve.md) Se **a** reserva não tiver sido emitida, a unidade padrão e o diretório serão aqueles associados à tarefa do aplicativo. Se um caminho for especificado, o dispositivo poderá exigir que ele seja na unidade de disco especificada pela reserva explícita ou **implícita.** Esse sinalizador é necessário. |
| keepreserve    | Especifica que o espaço em disco não usuário deixado do comando de **reserva** original não está desalocado.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

A *variável filename* será necessária se o dispositivo tiver sido aberto usando o identificador de dispositivo "novo".

## <a name="examples"></a>Exemplos

O comando a seguir salva todo o buffer de vídeo em um arquivo chamado VCAPFILE. Tga.

``` syntax
save vboard c:\vcap\vcapfile.tga
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

[Capturar](capture.md)
</dt> <dt>

[Reserva](reserve.md)
</dt> </dl>

 

