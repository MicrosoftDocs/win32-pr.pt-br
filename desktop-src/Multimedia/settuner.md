---
title: comando setajuster
description: O comando setajustarr altera o sintonizador atual ou a configuração de canal do sintonizador atual. Os dispositivos VCR reconhecem este comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- Multimídia do Windows do comando setajuster
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456030"
---
# <a name="settuner-command"></a>comando setajuster

O comando setajustarr altera o sintonizador atual ou a configuração de canal do sintonizador atual. Os dispositivos VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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
| *canal* de canal                | Define o sintonizador como *canal*. Talvez você não consiga alterar o canal durante a gravação, dependendo do VCR. Um canal maior do que o máximo define o sintonizador para o canal máximo.                                                                                                                    |
| busca de upchannel de busca de canal | Procura o próximo canal com um sinal válido. "Procurar" incrementa o número de canal em sua pesquisa. "Busca inativa" Decrementa o número do canal em sua pesquisa. O sintonizador encapsula para o canal 1 quando o número máximo do canal é excedido. Da mesma forma, ao procurar, o sintonizador é ajustado para o canal máximo. |
| upchannel do canal inativo           | Incrementa ou Decrementa o canal do sintonizador. Talvez você não consiga alterar o canal durante a gravação, dependendo do VCR. O sintonizador encapsula para o canal 1 quando o número máximo do canal é excedido. Da mesma forma, ao procurar, o sintonizador é ajustado para o canal máximo.                              |
| *número* de número                  | Especifica o sintonizador a ser afetado pelo comando setajuster. Se *núm* não for fornecido, o valor padrão de 1 será assumido.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

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
</dt> </dl>

 

