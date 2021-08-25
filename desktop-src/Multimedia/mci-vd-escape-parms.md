---
title: Estrutura de MCI_VD_ESCAPE_PARMS (Mciapi. h)
description: A estrutura de parâmetros de escape de VD do MCI \_ \_ \_ contém o comando enviado a um dispositivo para o \_ comando de escape MCI para dispositivos VIDEODISC.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- estrutura de MCI_VD_ESCAPE_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f9a0fef0e60168d4539756c741527d751fd726ab3d2472cdbaf3b080784e70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783841"
---
# <a name="mci_vd_escape_parms-structure"></a>\_Estrutura de \_ parâmetros de escape de VD do MCI \_

A estrutura de parâmetros de escape de VD do MCI contém o comando enviado a um dispositivo para o comando de [**\_ escape MCI**](mci-escape.md) para dispositivos VIDEODISC. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**lpstrCommand**
</dt> <dd>

Comando a ser enviado ao dispositivo.

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

[**\_escape MCI**](mci-escape.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

