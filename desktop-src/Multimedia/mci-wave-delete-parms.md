---
title: Estrutura de MCI_WAVE_DELETE_PARMS (Mciapi. h)
description: A estrutura de parâmetros de exclusão de Wave do MCI \_ \_ \_ contém informações de posição para o \_ comando MCI Delete para dispositivos de forma de onda-áudio.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- Multimídia do Windows da estrutura de MCI_WAVE_DELETE_PARMS
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454802"
---
# <a name="mci_wave_delete_parms-structure"></a>\_Estrutura de \_ parâmetros de exclusão de onda MCI \_

A estrutura de parâmetros de exclusão de Wave do MCI contém informações de posição para o comando [**MCI \_ delete**](mci-delete.md) para dispositivos de forma de onda-áudio. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posição da qual excluir.

</dd> <dt>

**dwTo**
</dt> <dd>

Posição para a qual excluir.

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

[**exclusão de MCI \_**](mci-delete.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

