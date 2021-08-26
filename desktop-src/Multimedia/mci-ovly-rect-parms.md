---
title: MCI_OVLY_RECT_PARMS (Mciapi.h)
description: A estrutura MCI OVLY RECT PARMS contém informações de posicionamento para os comandos MCI PUT e \_ \_ \_ \_ MCI \_ WHERE para dispositivos de sobreposição de vídeo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS estrutura Windows Multimídia
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
ms.openlocfilehash: 5cfd55b2950f6d4268a9af5ee5bdc7fc9c378c4dbaeaa569406339263a2cf85e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039106"
---
# <a name="mci_ovly_rect_parms-structure"></a>Estrutura MCI \_ OVLY \_ RECT \_ PARMS

A **estrutura MCI \_ OVLY \_ RECT \_ PARMS** contém informações de posicionamento para os comandos [**MCI \_ PUT**](mci-put.md) e [**MCI \_ WHERE**](mci-where.md) para dispositivos de sobreposição de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**Rc**
</dt> <dd>

Retângulo que contém informações de posicionamento. [As estruturas RECT](/previous-versions//ms536136(v=vs.85)) são tratadas de maneira diferente na MCI do que em outras partes do Windows; na MCI, **rc.right** contém a largura do retângulo e **rc.bottom contém** sua altura.

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

[**MCI \_ PUT**](mci-put.md)
</dt> <dt>

[**MCI \_ WHERE**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[Rect](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

