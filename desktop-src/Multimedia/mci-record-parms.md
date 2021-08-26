---
title: MCI_RECORD_PARMS (Mciapi.h)
description: A estrutura \_ \_ MCI RECORD PARMS contém informações de posicionamento para o comando MCI \_ RECORD.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c531b5b186a6119a22cafc4e252424ace2e388b2545461b440cd7957694494b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039076"
---
# <a name="mci_record_parms-structure"></a>Estrutura DO \_ \_ PARMS de REGISTRO MCI

A **estrutura \_ MCI RECORD \_ PARMS** contém informações de posicionamento para o [**comando MCI \_ RECORD.**](mci-record.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
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

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**REGISTRO \_ MCI**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

