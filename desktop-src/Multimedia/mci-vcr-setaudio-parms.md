---
title: Estrutura de MCI_VCR_SETAUDIO_PARMS (VCR. h)
description: A estrutura do MCI de \_ SetAudio de videocassetes \_ \_ contém parâmetros para o \_ comando de SetAudio do MCI para gravadores de vídeo-fita.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- estrutura de MCI_VCR_SETAUDIO_PARMS Windows multimídia
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
# <a name="mci_vcr_setaudio_parms-structure"></a>\_Estrutura de \_ parâmetros de áudio \_ MCI de VCR

A estrutura do **MCI de \_ \_ SetAudio \_ de videocassetes** contém parâmetros para o comando de [**\_ SetAudio do MCI**](mci-setaudio.md) para gravadores de vídeo-fita.

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

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

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

Entrada de áudio (do tipo especificado no membro **dwTo** ) a ser usado.

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

[**\_áudio MCI**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

