---
title: MCI_VCR_RECORD_PARMS estrutura (Vcr.h)
description: A estrutura PARMS de REGISTRO DE VCR da MCI contém parâmetros para o comando \_ \_ \_ MCI RECORD para gravadores de gravação de \_ vídeo.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b613c2b64bae1395b3fc402816145c0ef690801b9fd6402201198f7ff28a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038226"
---
# <a name="mci_vcr_record_parms-structure"></a>Estrutura \_ \_ PARMS de REGISTRO DE VCR da MCI \_

A **estrutura \_ \_ \_ PARMS** de REGISTRO DE VCR da MCI contém parâmetros para o comando [**MCI \_ RECORD**](mci-record.md) para gravadores de gravação de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
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

Valor de hora que afeta o [**comando MCI \_ RECORD**](mci-record.md) ou [**MCI \_ CUE.**](mci-cue.md) Para **REGISTRO \_ de MCI,** esta é a hora em que a gravação começa. Para **MCI \_ CUE**, esta é a hora em que o dispositivo cued atinge a posição determinada em **dwFrom**.

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

[**REGISTRO \_ MCI**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

