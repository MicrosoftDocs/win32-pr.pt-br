---
title: comando step
description: O comando de etapa etapas a reproduzir um ou mais quadros para frente ou para trás. A ação padrão é avançar um quadro. Os dispositivos video,VCR e videodisc no formato DIGITAL reconhecem esse comando.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- comando step Windows Multimídia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b804ac64c2641ba1eb43ba7019ae2668c04a7d8b07fbfd20ab7b8cb570d8fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370826"
---
# <a name="step-command"></a>comando step

O comando de etapa etapas a reproduzir um ou mais quadros para frente ou para trás. A ação padrão é avançar um quadro. Os dispositivos video,VCR e videodisc no formato DIGITAL reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*
</dt> <dd>

Um ou ambos os sinalizadores a seguir.



| Valor       | Significado                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| por *quadros* | Indica o número de quadros a ser etapa. Se você especificar um valor *de quadros negativos,* não poderá especificar o sinalizador "reverso". |
| reverse     | Estornar os quadros em ordem inversa.                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

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
</dt> </dl>

 

