---
description: Contém informações de formato para recompactação inteligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Estrutura SCompFmt0 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f02c9cda80acdd42d0687502834a9b2e66f1cf773d02b88eadabdd346850061e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072700"
---
# <a name="scompfmt0-structure"></a>Estrutura SCompFmt0

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Contém informações de formato para recompactação inteligente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nformatid**
</dt> <dd>

Reservado; deve ser zero.

</dd> <dt>

**MediaType**
</dt> <dd>

[**AM \_ Estrutura \_ MEDIA TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que descreve o formato de compactação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




