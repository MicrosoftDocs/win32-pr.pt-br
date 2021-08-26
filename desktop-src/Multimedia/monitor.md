---
title: comando monitorar
description: O comando monitor especifica a origem da apresentação. (A fonte de apresentação padrão é o espaço de trabalho.) Alternar a origem da apresentação alterna todos os fluxos de áudio e vídeo na origem. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- Windows de comando monitorar multimídia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef9a47db68856196dc84aefb3c5f110941189dec80f62b369eae13c60932d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038806"
---
# <a name="monitor-command"></a>comando monitorar

O comando monitor especifica a origem da apresentação. (A fonte de apresentação padrão é o espaço de trabalho.) Alternar a origem da apresentação alterna todos os fluxos de áudio e vídeo na origem. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Um ou mais dos sinalizadores a seguir.



| Valor           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file            | Especifica que o espaço de trabalho é a fonte da apresentação. Essa é a origem padrão.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Especifica que a entrada externa é a origem da apresentação. Se um comando [Play](play.md) estiver em andamento, primeiro será pausado. Se [setvideo](setvideo.md) for "on", esse sinalizador exibirá uma janela oculta padrão. Os dispositivos podem limitar o que outras instâncias de dispositivo podem fazer ao monitorar a entrada.                                                                                                                                                                                                                                                                                                                                                                    |
| *método* de método | Quando usado com o **Monitor** "Input", esse sinalizador seleciona o método de monitoramento. O *método* é "pre", "post" ou "Direct". Solicitações de monitoramento direto que o dispositivo está configurado para a qualidade de exibição ideal durante o monitoramento. O método de monitoramento direto pode ser incompatível com a gravação de vídeo de movimento. Pré e pós-monitoramento permitem a gravação do vídeo em movimento. O monitoramento prévio mostra a entrada externa antes da compactação, enquanto o pós-processamento mostra a entrada externa após a compactação. Normalmente, diferentes métodos de monitoramento têm diferentes implicações de hardware. O método de monitoramento padrão é selecionado pelo dispositivo.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A origem da apresentação alterna automaticamente para o espaço de trabalho após uma [reprodução](play.md), [etapa](step.md), [Pausar](pause.md), [indicação](cue.md) de "saída" ou comando de [busca](seek.md) . O comando [gravar](record.md) não alterna automaticamente as fontes de apresentação, o que dá ao aplicativo a opção de não mostrar o vídeo enquanto ele está sendo gravado.

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

[marcar](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[reproduzir](play.md)
</dt> <dt>

[gravável](record.md)
</dt> <dt>

[Procure](seek.md)
</dt> <dt>

[etapa](step.md)
</dt> </dl>

 

