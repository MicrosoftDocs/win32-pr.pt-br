---
title: MCI_VCR_SET_PARMS estrutura (Vcr.h)
description: A estrutura MCI VCR SET PARMS contém parâmetros para o \_ \_ comando \_ MCI SET para gravadores de gravação de \_ vídeo.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe32f93500ae4c294bad372868e9f7818c672824611bcbc29c3315eb75a9742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802981"
---
# <a name="mci_vcr_set_parms-structure"></a>Estrutura MCI \_ VCR \_ SET \_ PARMS

A **estrutura MCI \_ VCR SET \_ \_ PARMS** contém parâmetros para o [**comando MCI \_ SET**](mci-set.md) para gravadores de gravação de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora atual.

</dd> <dt>

**dwAudio**
</dt> <dd>

Não usado.

</dd> <dt>

**dwTimeMode**
</dt> <dd>

Constante que especifica a origem de tempo usada pelo dispositivo. A origem de tempo é um código-hora registrado na fita ou os contadores no dispositivo que sentem movimento de movimento de movimento.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Taxa de gravação.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Formato de um novo valor de hora do contador.

</dd> <dt>

**Dwindex**
</dt> <dd>

Conteúdo da exibição na tela.

</dd> <dt>

**dwTracking**
</dt> <dd>

Ajuste de velocidade usado ao acompanhar a taxa de reprodução de VCR.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidade de reprodução usada pelo dispositivo como um inteiro. A velocidade de reprodução normal é 1000, a velocidade dupla é 2000 e a metade da velocidade é de 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Comprimento da casa quando o comprimento não é detectável pelo dispositivo.

</dd> <dt>

**dwCounter**
</dt> <dd>

Novo valor do contador.

</dd> <dt>

**dwClock**
</dt> <dd>

Nova hora do relógio.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Novo valor de tempo-máximo para o comando pause.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Comprimento da fita necessário para estabilizar a saída do VCR.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Comprimento da fita necessário para interromper o transporte do VCR quando um [**comando MCI \_ STOP**](mci-stop.md) ou [**MCI \_ PAUSE**](mci-pause.md) é emitido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**PAUSA DA \_ MCI**](mci-pause.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**MCI \_ STOP**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

