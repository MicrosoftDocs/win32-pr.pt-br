---
title: Estrutura de MCI_OVLY_RECT_PARMS (Mciapi. h)
description: A estrutura do MCI \_ OVLY \_ Rect \_ parms contém informações de posicionamento para o MCI \_ Put e o MCI \_ , onde os comandos para dispositivos de sobreposição de vídeo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_RECT_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454605"
---
# <a name="mci_ovly_rect_parms-structure"></a>Estrutura de parâmetros do MCI \_ OVLY \_ Rect \_

A estrutura do **MCI \_ OVLY \_ Rect \_ parms** contém informações de posicionamento para o MCI [**\_ Put**](mci-put.md) e o [**MCI, \_ onde**](mci-where.md) os comandos para dispositivos de sobreposição de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**RC**
</dt> <dd>

Retângulo que contém informações de posicionamento. As estruturas [Rect](/previous-versions//ms536136(v=vs.85)) são tratadas de forma diferente no MCI do que em outras partes do Windows; no MCI, **RC. Right** contém a largura do retângulo e **RC. Bottom** contém sua altura.

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

[**\_Put MCI**](mci-put.md)
</dt> <dt>

[**MCI \_ onde**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECT](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

