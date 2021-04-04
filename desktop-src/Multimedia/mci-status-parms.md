---
title: Estrutura de MCI_STATUS_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de status MCI \_ contém informações para o \_ comando status MCI.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Multimídia do Windows da estrutura de MCI_STATUS_PARMS
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
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918104"
---
# <a name="mci_status_parms-structure"></a>Estrutura de parâmetros de \_ status do MCI \_

A estrutura de **\_ \_ parâmetros de status MCI** contém informações para o comando [**\_ status MCI**](mci-status.md) .

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

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contém informações sobre o retorno.

</dd> <dt>

**dwItem**
</dt> <dd>

Funcionalidade que está sendo consultada.

</dd> <dt>

**dwTrack**
</dt> <dd>

Comprimento ou número de faixas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ sinalizador de item de status MCI \_ deve ser definido no parâmetro *FdwCommand* da função [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar o membro **dwItem** , que deve conter uma das constantes que indicam quais informações de status estão sendo solicitadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**STATUS do MCI \_**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

