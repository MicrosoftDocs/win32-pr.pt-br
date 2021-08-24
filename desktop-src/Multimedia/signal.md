---
title: comando signal
description: O comando signal identifica uma posição especificada no workspace enviando ao aplicativo uma mensagem MM \_ MCISIGNAL. Os dispositivos de vídeo digital reconhecem esse comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- comando signal Windows Multimídia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db007a03738f13bb9acc0733b67bcd38de4b97f2b194bb16cdfcd85f798cfdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037176"
---
# <a name="signal-command"></a>comando signal

O comando signal identifica uma posição especificada no workspace enviando ao aplicativo uma [mensagem MM \_ MCISIGNAL.](mm-mcisignal.md) Os dispositivos de vídeo digital reconhecem esse comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

Um dos sinalizadores a seguir.



| Valor            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| na posição      | Especifica o quadro para invocar um sinal.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | Remove sinais do workspace. Um sinal individual é especificado usando o sinalizador "uservalue". Se o sinalizador "uservalue" não for especificado usando "cancelar", o dispositivo cancelará todos os sinais. O sinalizador "cancelar" é incompatível com os sinalizadores "at", "every" e "return position".                                                                                                                                                                                                                                                                                          |
| a cada *intervalo* | Especifica o período dos sinais. O *valor* do intervalo é especificado no formato de hora atual. Se usado com a posição "at", os sinais serão colocados em todo o workspace com uma marca de sinal colocada na *posição*.<br/> Sem o sinalizador "at", os sinais são colocados em todo o workspace com um sinal na posição atual.<br/> Se esse sinalizador for omitido, somente a posição indicada pelo sinalizador "at" será marcada.<br/> Se o *valor de* intervalo for menor que a frequência mínima com suporte de um dispositivo, ele usará seu valor mínimo.<br/> |
| posição de retorno  | Indica que o dispositivo deve enviar o valor da posição em vez do identificador "uservalue" na mensagem de sinalização. O identificador "uservalue" ainda pode ser usado para cancelar ou redefinir as marcas de sinal.                                                                                                                                                                                                                                                                                                                                                                      |
| id  uservalue   | Especifica um identificador que é relatado novamente com a mensagem de sinalização. Esse identificador atua como um identificador que pode ser usado com outros comandos **de** sinal para referenciar essa **configuração de** sinal. Se omitido, o valor padrão será zero.                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify", "test" ou uma combinação deles. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O alça de janela usado para notificação de mensagens de conclusão de comando também é usado para sinalização.

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

[MM \_ MCISIGNAL](mm-mcisignal.md)
</dt> </dl>

 

