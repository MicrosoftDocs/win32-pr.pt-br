---
title: Estrutura de MCI_GENERIC_PARMS (Mciapi. h)
description: A \_ \_ estrutura de parâmetros genéricos do MCI contém o identificador da janela que recebe mensagens de notificação. Essa estrutura é usada para mensagens de comando MCI que têm listas de parâmetros vazias.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Multimídia do Windows da estrutura de MCI_GENERIC_PARMS
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454984"
---
# <a name="mci_generic_parms-structure"></a>\_Estrutura de parâmetros genéricos do MCI \_

A estrutura de **\_ \_ parâmetros genéricos do MCI** contém o identificador da janela que recebe mensagens de notificação. Essa estrutura é usada para mensagens de comando MCI que têm listas de parâmetros vazias.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> </dl>

## <a name="remarks"></a>Comentários

As estruturas dos parâmetros de **\_ fechamento \_ MCI** e **MCI \_ percebem \_ parâmetros** são idênticas à estrutura de **\_ \_ parâmetros genéricos do MCI** .

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

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

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

