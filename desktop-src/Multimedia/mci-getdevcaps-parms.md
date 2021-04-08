---
title: Estrutura de MCI_GETDEVCAPS_PARMS (Mciapi. h)
description: A estrutura do MCI \_ GETDEVCAPS \_ parms contém informações de capacidade de dispositivo para o \_ comando GETDEVCAPS MCI.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Multimídia do Windows da estrutura de MCI_GETDEVCAPS_PARMS
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009061"
---
# <a name="mci_getdevcaps_parms-structure"></a>\_Estrutura do GETDEVCAPS \_ parms de MCI

A estrutura do **MCI \_ GETDEVCAPS \_ parms** contém informações de capacidade de dispositivo para o comando [**\_ GETDEVCAPS MCI**](mci-getdevcaps.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contém informações sobre a saída.

</dd> <dt>

**dwItem**
</dt> <dd>

Funcionalidade que está sendo consultada. Esse membro pode ser uma das constantes listadas no material de referência para o comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

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

[**\_GETDEVCAPS MCI**](mci-getdevcaps.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

