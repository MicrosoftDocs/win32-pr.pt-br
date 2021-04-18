---
description: Contém informações de formato para a recompactação inteligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Estrutura SCompFmt0 (QEdit. h)
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
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758428"
---
# <a name="scompfmt0-structure"></a>Estrutura SCompFmt0

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Contém informações de formato para a recompactação inteligente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Membros

<dl> <dt>

**nFormatId**
</dt> <dd>

Reservado deve ser zero.

</dd> <dt>

**MediaType**
</dt> <dd>

[**Am \_ Estrutura do \_ tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type) que descreve o formato de compactação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




