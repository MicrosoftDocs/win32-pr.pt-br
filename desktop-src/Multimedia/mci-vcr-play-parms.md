---
title: Estrutura de MCI_VCR_PLAY_PARMS (VCR. h)
description: A estrutura do MCI de \_ reprodução de videocassetes \_ \_ contém parâmetros para o \_ comando de reprodução MCI para gravadores de fita de vídeo.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_PLAY_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918557"
---
# <a name="mci_vcr_play_parms-structure"></a>\_Estrutura de \_ parâmetros de reprodução de VCR MCI \_

A estrutura do **MCI de \_ \_ reprodução \_ de videocassetes** contém parâmetros para o comando de [**\_ reprodução MCI**](mci-play.md) para gravadores de fita de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posição da qual reproduzir.

</dd> <dt>

**dwTo**
</dt> <dd>

Posição para reprodução.

</dd> <dt>

**dwAt**
</dt> <dd>

Valor de tempo que afeta o comando [**MCI \_ Play**](mci-play.md) ou [**MCI \_ Cue**](mci-cue.md) . Para [**\_ reprodução MCI**](mci-play-parms.md), esse é o momento em que a reprodução é iniciada. Para **a \_ indicação de MCI**, essa é a hora em que o dispositivo cued atinge a posição fornecida em **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Comentários

As posições são especificadas no formato de hora atual.

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

[**indicação de MCI \_**](mci-cue.md)
</dt> <dt>

[**\_reprodução MCI**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

