---
title: Estrutura de MCI_WAVE_SET_PARMS (Mciapi. h)
description: A \_ estrutura de \_ \_ parâmetros Set parms do MCI contém informações para o \_ comando set do MCI para dispositivos de forma de onda-áudio.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- estrutura de MCI_WAVE_SET_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85508ec493ecdc38825b90877e608683fe6c0bb7c099365c187a434890c605d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783746"
---
# <a name="mci_wave_set_parms-structure"></a>\_Estrutura de \_ parâmetros do conjunto de ondas MCI \_

A estrutura de **\_ \_ \_ parâmetros Set parms do MCI** contém informações para o comando [**\_ set do MCI**](mci-set.md) para dispositivos de forma de onda-áudio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora do dispositivo.

</dd> <dt>

**dwAudio**
</dt> <dd>

Número de canal para saída de áudio. Normalmente usado ao ativar ou desativar um canal.

</dd> <dt>

**wInput**
</dt> <dd>

Canal de entrada de áudio.

</dd> <dt>

**wOutput**
</dt> <dd>

Dispositivo de saída a ser usado. Por exemplo, esse valor poderia ser 2 se um sistema tiver duas placas de som instaladas.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Formato dos dados de wave-áudio, como PCM de \_ formato Wave \_ . Os valores possíveis são definidos em Mmreg. h.

</dd> <dt>

**wReserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**nChannels**
</dt> <dd>

Mono (1) ou estéreo (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Reservado.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Exemplos por segundo.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Taxa de amostragem em bytes por segundo.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Bloquear o alinhamento dos dados.

</dd> <dt>

**wReserved4**
</dt> <dd>

Reservado.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por amostra.

</dd> <dt>

**wReserved5**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**conjunto de MCI \_**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

