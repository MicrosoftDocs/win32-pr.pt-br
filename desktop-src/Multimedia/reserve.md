---
title: comando Reserve
description: O comando Reserve aloca espaço em disco contíguo para o espaço de trabalho da instância do dispositivo. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando de reserva de multimídia do Windows
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918012"
---
# <a name="reserve-command"></a>comando Reserve

O comando Reserve aloca espaço em disco contíguo para o espaço de trabalho da instância do dispositivo. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

Um ou mais dos sinalizadores a seguir.



| Valor           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *caminho*       | Especifica a unidade e o caminho do diretório (mas não o nome) de um arquivo temporário usado para armazenar dados gravados. O nome desse arquivo é especificado pelo dispositivo. O arquivo temporário é excluído quando o dispositivo é fechado. Se esse sinalizador for omitido, o dispositivo especificará o local do espaço em disco.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *duração* do tamanho | Especifica a quantidade aproximada de espaço em disco a ser reservada no espaço de trabalho. O valor *Duration* é especificado no formato de hora atual. O dispositivo baseia sua estimativa do espaço em disco necessário nos seguintes parâmetros: a hora solicitada, o formato de arquivo, o algoritmo de compactação de vídeo e áudio e os valores de qualidade de compactação em vigor. Se [setvideo](setvideo.md) "registro" for "desativado", o espaço será reservado somente para áudio. Se [SetAudio](setaudio.md) "registro" for "desativado", o espaço será reservado somente para vídeo. Se ambos estiverem "desativados" ou se a *duração* for zero, nenhum espaço será reservado e qualquer espaço reservado existente será desalocado. Se esse sinalizador for omitido, o dispositivo usará um padrão definido pelo dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se necessário, os comandos [gravar](record.md) ou [salvar](save.md) subsequentes usam o espaço reservado por esse comando. Se o espaço de trabalho contiver dados não salvos, os dados serão perdidos. Alguns dispositivos não exigem reserva e os ignoram. Se o espaço em disco não for reservado antes da gravação, o comando gravar executará uma reserva implícita com sinalizadores padrão específicos do dispositivo. Use um comando de reserva explícito se desejar um melhor controle de quando ocorrer o atraso de alocação de disco, o controle de quanto espaço é alocado e o controle de onde o espaço em disco é alocado. Seu aplicativo pode alterar a quantidade e o local do espaço em disco reservado anteriormente com os comandos de reserva subsequentes. Qualquer espaço em disco alocado e ainda não utilizado não será desalocado até que os dados gravados sejam salvos ou até que a instância do dispositivo seja fechada.

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

[gravável](record.md)
</dt> <dt>

[salvar](save.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

