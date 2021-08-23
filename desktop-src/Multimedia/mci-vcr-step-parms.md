---
title: MCI_VCR_STEP_PARMS estrutura (Vcr.h)
description: A estrutura MCI VCR STEP PARMS contém parâmetros para o comando \_ \_ \_ MCI \_ STEP para gravadores de gravação de vídeo.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS estrutura Windows Multimídia
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
ms.openlocfilehash: 7f25e79903a694b6537e88d1c58994d1f39ccf958ea95f40f571a267239a055e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783821"
---
# <a name="mci_vcr_step_parms-structure"></a>Estrutura DO \_ \_ PARMS de ETAPA DO \_ VCR da MCI

A **estrutura MCI \_ VCR STEP \_ \_ PARMS** contém parâmetros para o comando [**MCI \_ STEP**](mci-step.md) para gravadores de gravação de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**dwFrames**
</dt> <dd>

Número de quadros a serem saltadas (o comprimento de uma única etapa) conforme o comando [**MCI \_ STEP**](mci-step.md) avança ou retrocede pelo conteúdo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros nessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* [**de mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

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

[**ETAPA da \_ MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

