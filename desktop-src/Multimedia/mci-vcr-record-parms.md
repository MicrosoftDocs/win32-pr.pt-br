---
title: Estrutura de MCI_VCR_RECORD_PARMS (VCR. h)
description: A estrutura de parâmetros de \_ registro de VCR MCI \_ \_ contém parâmetros para o \_ comando de registro MCI para gravadores de vídeo-fita.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_RECORD_PARMS
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
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759200"
---
# <a name="mci_vcr_record_parms-structure"></a>\_Estrutura de \_ parâmetros de registro de VCR MCI \_

A estrutura de parâmetros de **\_ registro de VCR \_ \_ MCI** contém parâmetros para o comando de [**\_ registro MCI**](mci-record.md) para gravadores de vídeo-fita.

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

Valor de tempo que afeta [**o \_ registro MCI**](mci-record.md) ou o comando de [**\_ indicação MCI**](mci-cue.md) . Para **o \_ registro MCI**, esse é o momento em que a gravação começa. Para **a \_ indicação de MCI**, essa é a hora em que o dispositivo cued atinge a posição fornecida em **dwFrom**.

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

[**\_registro MCI**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

