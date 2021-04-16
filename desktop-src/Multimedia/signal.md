---
title: comando de sinal
description: O comando Signal identifica uma posição especificada no espaço de trabalho enviando o aplicativo uma \_ mensagem mm MCISIGNAL. Dispositivos de vídeo digital reconhecem este comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Multimídia do Windows de comando de sinal
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779613"
---
# <a name="signal-command"></a>comando de sinal

O comando Signal identifica uma posição especificada no espaço de trabalho enviando o aplicativo uma mensagem [mm \_ MCISIGNAL](mm-mcisignal.md) . Dispositivos de vídeo digital reconhecem este comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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
| cancel           | Remove os sinais do espaço de trabalho. Um sinal individual é especificado usando o sinalizador "uservalue". Se o sinalizador "uservalue" não for especificado com o uso de "Cancel", o dispositivo cancelará todos os sinais. O sinalizador "Cancelar" é incompatível com os sinalizadores "at", "todos" e "posição de retorno".                                                                                                                                                                                                                                                                                          |
| cada *intervalo* | Especifica o período dos sinais. O valor do *intervalo* é especificado no formato de hora atual. Se usado com a *posição*"at", os sinais são colocados em todo o espaço de trabalho com uma marca de sinal colocada na *posição*.<br/> Sem o sinalizador "at", os sinais são colocados em todo o espaço de trabalho com um sinal na posição atual.<br/> Se esse sinalizador for omitido, somente a posição indicada pelo sinalizador "at" será marcada.<br/> Se o valor do *intervalo* for menor que a frequência mínima com suporte de um dispositivo, ele usará seu valor mínimo.<br/> |
| posição de retorno  | Indica que o dispositivo deve enviar o valor de posição em vez do identificador "uservalue" na mensagem de sinalização. O identificador "uservalue" ainda pode ser usado para cancelar ou redefinir as marcas de sinalização.                                                                                                                                                                                                                                                                                                                                                                      |
| *ID* de uservalue   | Especifica um identificador que é relatado de volta com a mensagem de sinalização. Esse identificador atua como um identificador que pode ser usado com outros comandos de **sinal** para fazer referência a essa configuração de **sinal** . Se omitido, o valor padrão será zero.                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O identificador de janela usado para notificação de mensagens de conclusão de comando também é usado para sinalização.

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

[\_MCISIGNAL mm](mm-mcisignal.md)
</dt> </dl>

 

