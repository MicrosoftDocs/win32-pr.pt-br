---
title: Estrutura de MCI_VCR_SET_PARMS (VCR. h)
description: A \_ estrutura do VCR do conjunto de videocassetes do MCI \_ \_ contém parâmetros para o \_ comando set do MCI para gravadores de vídeo-fita.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SET_PARMS
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
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369856"
---
# <a name="mci_vcr_set_parms-structure"></a>\_Estrutura de \_ parâmetros de conjunto de VCR MCI \_

A estrutura do **\_ VCR do \_ conjunto \_ de videocassetes do MCI** contém parâmetros para o comando [**\_ set do MCI**](mci-set.md) para gravadores de vídeo-fita.

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

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

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

Constante que especifica a fonte de tempo usada pelo dispositivo. A origem de temporização é um código de tempo registrado em fita de vídeo ou os contadores no dispositivo que detectam a movimentação da fita.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Taxa de gravação.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Formato de um novo valor de hora do contador.

</dd> <dt>

**dwIndex**
</dt> <dd>

Conteúdo da exibição na tela.

</dd> <dt>

**dwTracking**
</dt> <dd>

Ajuste de velocidade usado ao acompanhar a taxa de reprodução de VCR.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidade de reprodução usada pelo dispositivo como um inteiro. A velocidade de reprodução normal é 1000, a velocidade dupla é 2000 e a meia velocidade é 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Tamanho da fita quando o comprimento não puder ser detectado pelo dispositivo.

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

Novo valor de tempo limite para o comando de pausa.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Tamanho da fita de vídeo necessário para estabilizar a saída do VCR.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Tamanho da fita de vídeo necessário para [**\_ finalizar**](mci-stop.md) o transporte de videocassete quando um comando Stop MCI ou [**MCI \_ Pause**](mci-pause.md) é emitido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**pausa de MCI \_**](mci-pause.md)
</dt> <dt>

[**conjunto de MCI \_**](mci-set.md)
</dt> <dt>

[**parada do MCI \_**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

