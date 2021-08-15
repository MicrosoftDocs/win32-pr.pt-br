---
title: MCI_VCR_PLAY_PARMS (Vcr.h)
description: A estrutura MCI \_ VCR PLAY PARMS contém parâmetros para o \_ \_ comando MCI PLAY para gravadores de gravação de \_ vídeo.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS estrutura Windows Multimídia
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
ms.openlocfilehash: 6f2e725ca3dc04fa13dd89aff0a5fbd60ede66f83154740803c98679eb77aec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374351"
---
# <a name="mci_vcr_play_parms-structure"></a>Estrutura MCI \_ VCR \_ PLAY \_ PARMS

A **estrutura MCI \_ VCR PLAY \_ \_ PARMS** contém parâmetros para o [**comando MCI \_ PLAY**](mci-play.md) para gravadores de gravação de vídeo.

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

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**Dwfrom**
</dt> <dd>

Posição da onde reproduzir.

</dd> <dt>

**dwTo**
</dt> <dd>

Posição para a reprodução.

</dd> <dt>

**dwAt**
</dt> <dd>

Valor de tempo que afeta o [**comando MCI \_ PLAY**](mci-play.md) ou [**MCI \_ CUE.**](mci-cue.md) Para [**MCI \_ PLAY,**](mci-play-parms.md)essa é a hora em que a reprodução começa. Para **MCI \_ CUE**, esta é a hora em que o dispositivo cued atinge a posição determinada em **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Comentários

As posições são especificadas no formato de hora atual.

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

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

