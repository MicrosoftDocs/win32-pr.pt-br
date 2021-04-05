---
title: Estrutura de MCI_SEQ_SET_PARMS (Mciapi. h)
description: A estrutura do MCI \_ Seq \_ set \_ parms contém informações para o \_ comando set do MCI para dispositivos do Sequencer MIDI.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Multimídia do Windows da estrutura de MCI_SEQ_SET_PARMS
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
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918105"
---
# <a name="mci_seq_set_parms-structure"></a>\_Estrutura do \_ conjunto de \_ parâmetros do MCI Seq

A estrutura do **MCI \_ Seq \_ set \_ parms** contém informações para o comando [**\_ set do MCI**](mci-set.md) para dispositivos do Sequencer MIDI.

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

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora do sequenciador.

</dd> <dt>

**dwAudio**
</dt> <dd>

Canal de saída de áudio.

</dd> <dt>

**dwTempo**
</dt> <dd>

Golpe.

</dd> <dt>

**dwPort**
</dt> <dd>

Porta.

</dd> <dt>

**dwSlave**
</dt> <dd>

Tipo de sincronização usado pelo Sequencer para a operação subordinada.

</dd> <dt>

**dwMaster**
</dt> <dd>

Tipo de sincronização usado pelo Sequencer para a operação mestre.

</dd> <dt>

**dwOffset**
</dt> <dd>

Deslocamento de dados.

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

 

