---
title: MCI_STATUS_PARMS (Mciapi.h)
description: A estrutura \_ PARMS DE STATUS \_ da MCI contém informações para o comando STATUS da \_ MCI.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2685ec70f10dc8dcecb0149f3bcf1af6c9814dd360e8f7e185d31710c24d5527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138092"
---
# <a name="mci_status_parms-structure"></a>Estrutura \_ PARMS DE STATUS da MCI \_

A **estrutura \_ \_ PARMS DE STATUS da MCI** contém informações para o [**comando \_ STATUS da MCI.**](mci-status.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contém informações sobre retorno.

</dd> <dt>

**dwItem**
</dt> <dd>

Capacidade que está sendo consultada.

</dd> <dt>

**dwTrack**
</dt> <dd>

Comprimento ou número de faixas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O sinalizador ITEM DE STATUS da MCI deve ser definido no parâmetro \_ \_ *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar o membro **dwItem,** que deve conter uma das constantes que indica quais informações de status estão sendo solicitadas.

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

[**STATUS DA MCI \_**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

