---
title: Estrutura de MCI_VD_STEP_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de etapa de VD do MCI \_ \_ contém informações para o \_ comando de etapa MCI para dispositivos VIDEODISC.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- Multimídia do Windows da estrutura de MCI_VD_STEP_PARMS
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499386"
---
# <a name="mci_vd_step_parms-structure"></a>\_Estrutura de \_ parâmetros da etapa de VD do MCI \_

A estrutura de parâmetros de etapa de VD do MCI contém informações para o comando de [**\_ etapa MCI**](mci-step.md) para dispositivos VIDEODISC. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwFrames**
</dt> <dd>

Número de quadros a serem conetapas.

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

[**\_etapa MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

