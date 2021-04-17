---
title: comando salvar
description: O comando salvar salva um arquivo MCI. Os dispositivos de sobreposição de vídeo e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não dão suporte a ele.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- salvar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812900"
---
# <a name="save-command"></a>comando salvar

O comando salvar salva um arquivo MCI. Os dispositivos de sobreposição de vídeo e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não dão suporte a ele.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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

Sinalizador que especifica o nome do arquivo que está sendo salvo e, opcionalmente, sinalizadores adicionais modificando a operação de salvamento. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **salvar** e os sinalizadores usados por cada tipo.



| Valor        | Significado              | Significado               |
|--------------|----------------------|-----------------------|
| digitalvideo | anular no *retângulo* | *nome do arquivo* keepreserve |
| overlay      | no *retângulo*       | *nome do arquivo*            |
| sequenciador    | *nome do arquivo*           |                       |
| waveaudio    | *nome do arquivo*           |                       |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszFileName** e seus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Interrompe uma operação de **salvamento** em andamento. Se usado, deve ser o único item presente.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| no *retângulo* | Especifica um retângulo relativo à origem do buffer do quadro. O *retângulo* é especificado como *X1 Y1 x2 y2*. As coordenadas *X1 Y1* especificam o canto superior esquerdo e as coordenadas *x2 y2* especificam a largura e a altura. Para dispositivos de vídeo digital, o comando de [captura](capture.md) é usado para capturar o conteúdo do buffer de quadro.<br/>                                                                                                                                               |
| *nome do arquivo*     | Especifica o nome de arquivo a ser atribuído ao arquivos de dados. Se um caminho não for especificado, o arquivo será colocado no disco e no diretório especificado anteriormente no comando [reserva](reserve.md) explícita ou implícita. Se a **reserva** não tiver sido emitida, a unidade e o diretório padrão serão os associados à tarefa do aplicativo. Se um caminho for especificado, o dispositivo poderá exigir que ele esteja na unidade de disco especificada pela **reserva** explícita ou implícita. Esse sinalizador é necessário. |
| keepreserve    | Especifica que o espaço em disco não utilizado restante do comando de **reserva** original não é desalocado.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A variável *filename* será necessária se o dispositivo tiver sido aberto usando o identificador de dispositivo "novo".

## <a name="examples"></a>Exemplos

O comando a seguir salva todo o buffer de vídeo em um arquivo chamado VCAPFILE. TGA.

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

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[captura](capture.md)
</dt> <dt>

[reservado](reserve.md)
</dt> </dl>

 

