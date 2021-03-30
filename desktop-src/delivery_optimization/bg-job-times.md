---
title: Estrutura de BG_JOB_TIMES (Deliveryoptimization. h)
description: A estrutura de BG_JOB_TIMES fornece carimbos de data/hora relacionados ao trabalho.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Estrutura de BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644355"
---
# <a name="bg_job_times-structure"></a>Estrutura de BG_JOB_TIMES

A estrutura de **BG_JOB_TIMES** fornece carimbos de data/hora relacionados ao trabalho.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>Membros

<dl> <dt>

**CreationTime**
</dt> <dd>

Hora em que o trabalho foi criado. A hora é especificada como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**Modificatime**
</dt> <dd>

Hora em que o trabalho foi modificado pela última vez ou os bytes foram transferidos. Adicionar arquivos ou chamar qualquer um dos métodos set nas interfaces [ * *método ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) altera esse valor. Além disso, as alterações no estado do trabalho e na chamada dos [métodos *_ suspender* *](ibackgroundcopyjob-suspend.md), [**retomar**](ibackgroundcopyjob-resume.md), [**Cancelar**](ibackgroundcopyjob-cancel.md)e [**concluir**](ibackgroundcopyjob-complete.md) alteram esse valor. A hora é especificada como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**TransferCompletionTime**
</dt> <dd>

Hora em que o trabalho entrou no estado de BG_JOB_STATE_TRANSFERRED. A hora é especificada como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Método ibackgroundcopyjob:: gettimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

