---
title: MCI_PLAY_PARMS (Mciapi.h)
description: A estrutura MCI \_ PLAY \_ PARMS contém informações de posicionamento para o comando MCI \_ PLAY.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- MCI_PLAY_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd45269cd74d15d2326bf4c6528d5778ef7a5a35e40dfd2a74134afafdbcb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803467"
---
# <a name="mci_play_parms-structure"></a>Estrutura MCI \_ PLAY \_ PARMS

A **estrutura MCI \_ PLAY \_ PARMS** contém informações de posicionamento para o [**comando MCI \_ PLAY.**](mci-play.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
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

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

