---
title: Comando settuner
description: O comando settuner altera o ajuste atual ou a configuração de canal do ajuste atual. Os dispositivos VCR reconhecem esse comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- Comando settuner Windows Multimídia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7075de6ed50c49773a502ba77e093d84e85b079a6b17c462ea8ee65ad1330aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688787"
---
# <a name="settuner-command"></a>Comando settuner

O comando settuner altera o ajuste atual ou a configuração de canal do ajuste atual. Os dispositivos VCR reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

Um dos sinalizadores a seguir.



| Valor                            | Significado                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| canal                 | Define o ajuste como *canal*. Talvez você não consiga alterar o canal durante a gravação, dependendo do VCR. Um canal maior que o máximo define o ajuste para o canal máximo.                                                                                                                    |
| channel seek upchannel seek down | Busca o próximo canal com um sinal válido. "Buscar para cima" incrementa o número do canal em sua pesquisa. "Buscar para baixo" diminui o número do canal em sua pesquisa. O ajuste é fechado para o canal 1 quando o número máximo do canal é excedido. Da mesma forma, ao buscar para baixo, o ajuste é fechado para o canal máximo. |
| canal upchannel para baixo           | Incrementa ou diminui o canal do ajuste. Talvez você não consiga alterar o canal durante a gravação, dependendo do VCR. O ajuste é fechado para o canal 1 quando o número máximo do canal é excedido. Da mesma forma, ao buscar para baixo, o ajuste é fechado para o canal máximo.                              |
| número *do número*                  | Especifica o ajuste a ser afetado pelo comando settuner. Se *number* não for determinado, o valor padrão de 1 será assumido.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify", "test" ou uma combinação deles. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

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

 

