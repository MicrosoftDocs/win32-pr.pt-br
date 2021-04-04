---
title: Estrutura de MCI_VCR_STEP_PARMS (VCR. h)
description: A \_ estrutura de parâmetros de etapa do VCR MCI \_ \_ contém parâmetros para o \_ comando de etapa MCI para gravadores de vídeo-fita.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_STEP_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008979"
---
# <a name="mci_vcr_step_parms-structure"></a>\_Estrutura de \_ parâmetros da etapa do VCR MCI \_

A estrutura de **\_ parâmetros de \_ etapa \_ do VCR MCI** contém parâmetros para o comando de [**\_ etapa MCI**](mci-step.md) para gravadores de vídeo-fita.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwFrames**
</dt> <dd>

Número de quadros para saltar (o comprimento de uma única etapa) conforme as etapas de comando da [**\_ etapa MCI**](mci-step.md) avançam ou regressivem pelo conteúdo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros nessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* de [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

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

[**\_etapa MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

