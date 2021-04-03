---
title: Estrutura de MCI_VCR_SETVIDEO_PARMS (VCR. h)
description: A estrutura de vídeo de VCR do MCI de \_ videocassete \_ \_ contém parâmetros para o comando do MCI \_ de vídeo para gravadores de vídeo-fita.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SETVIDEO_PARMS
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
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824702"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>\_Estrutura de \_ parâmetros de vídeo de VCR MCI \_

A estrutura de **vídeo de VCR do MCI de \_ videocassete \_ \_** contém parâmetros para o comando do MCI de vídeo para gravadores de vídeo-fita. [**\_**](mci-setvideo.md)

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

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwTrack**
</dt> <dd>

Controle afetado.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo de entrada ou entrada monitorada.

</dd> <dt>

**dwNumber**
</dt> <dd>

Entrada de vídeo (do tipo especificado no membro **dwTo** ) a ser usado.

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

[**VÍDEO do MCI \_**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

