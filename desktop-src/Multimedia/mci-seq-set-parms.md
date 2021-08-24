---
title: MCI_SEQ_SET_PARMS (Mciapi.h)
description: A estrutura MCI \_ SEQ \_ SET \_ PARMS contém informações para o comando MCI \_ SET para dispositivos de sequenciador MIDI.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffb96cfd2f652bf989673bad68c95c6765034d2105fa554efee057faf099a9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374964"
---
# <a name="mci_seq_set_parms-structure"></a>Estrutura MCI \_ SEQ \_ SET \_ PARMS

A **estrutura MCI \_ SEQ SET \_ \_ PARMS** contém informações para o [**comando MCI \_ SET**](mci-set.md) para dispositivos de sequenciador MIDI.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de tempo do Sequencer.

</dd> <dt>

**dwAudio**
</dt> <dd>

Canal de saída de áudio.

</dd> <dt>

**dwTempo**
</dt> <dd>

Tempo.

</dd> <dt>

**dwPort**
</dt> <dd>

Porta.

</dd> <dt>

**dw Ltda**
</dt> <dd>

Tipo de sincronização usado pelo sequenciador para a operação subordinada.

</dd> <dt>

**dwMaster**
</dt> <dd>

Tipo de sincronização usado pelo sequenciador para a operação mestra.

</dd> <dt>

**Dwoffset**
</dt> <dd>

Deslocamento de dados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

