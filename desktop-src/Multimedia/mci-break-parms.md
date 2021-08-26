---
title: Estrutura de MCI_BREAK_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de interrupção MCI contém o código de \_ chave virtual e as informações de janela do \_ comando MCI Break.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- estrutura de MCI_BREAK_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efaff8841e0e8ef0387535aa8d42723cf9477887511b7111f02a6ee0cb2b527b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039506"
---
# <a name="mci_break_parms-structure"></a>Estrutura de parâmetros de \_ interrupção MCI \_

A estrutura de **\_ \_ parâmetros de interrupção MCI** contém o código de chave virtual e as informações de janela do comando [**MCI \_ Break**](mci-break.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**nVirtKey**
</dt> <dd>

Código de chave virtual para chave de interrupção.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Identificador para a janela que deve ser a janela atual para detecção de interrupção.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros. Os seguintes sinalizadores são definidos:

\_HWND de interrupção de MCI \_

Valida o membro **hwndBreak** especificando a janela que deve ter foco para habilitar a detecção de interrupção.

\_chave de interrupção MCI \_

Valida o membro **nVirtKey** especificando o código de chave virtual a ser usado para a chave de interrupção.

interrupção do MCI \_ \_

Desabilita qualquer chave de quebra existente.

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

[**interrupção de MCI \_**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

