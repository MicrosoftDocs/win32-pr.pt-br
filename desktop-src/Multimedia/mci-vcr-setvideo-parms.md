---
title: MCI_VCR_SETVIDEO_PARMS estrutura (Vcr.h)
description: A estrutura MCI \_ VCR SETVIDEO PARMS contém parâmetros para o comando \_ \_ MCI \_ SETVIDEO para gravadores de gravação de vídeo.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf260804a6e993ba133ca450a51802a0f43db3aa3d0e557ba684b8a86bcfb7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784126"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>Estrutura MCI \_ VCR \_ SETVIDEO \_ PARMS

A **estrutura MCI \_ VCR \_ SETVIDEO \_ PARMS** contém parâmetros para o comando [**MCI \_ SETVIDEO**](mci-setvideo.md) para gravadores de gravação de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**dwTrack**
</dt> <dd>

Faixa afetada.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo de entrada ou entrada monitorada.

</dd> <dt>

**dwNumber**
</dt> <dd>

Entrada de vídeo (do tipo especificado no membro **dwTo)** a ser usada.

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

[**MCI \_ SETVIDEO**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

