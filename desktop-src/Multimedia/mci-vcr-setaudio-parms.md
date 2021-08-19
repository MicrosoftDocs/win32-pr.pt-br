---
title: MCI_VCR_SETAUDIO_PARMS estrutura (Vcr.h)
description: A estrutura MCI \_ VCR SETAUDIO PARMS contém parâmetros para o comando \_ \_ MCI SETAUDIO para gravadores de gravação \_ de vídeo.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa07d4cf8b88eb246019bf18dd1c1328413718a70b17ebb16e27606958473f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802954"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>Estrutura MCI \_ VCR \_ SETAUDIO \_ PARMS

A **estrutura MCI \_ VCR \_ SETAUDIO \_ PARMS** contém parâmetros para o comando [**MCI \_ SETAUDIO**](mci-setaudio.md) para gravadores de gravação de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**dwTrack**
</dt> <dd>

Faixa de áudio.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo de entrada ou entrada monitorada.

</dd> <dt>

**dwNumber**
</dt> <dd>

Entrada de áudio (do tipo especificado no membro **dwTo)** a ser usada.

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

[**MCI \_ SETAUDIO**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

