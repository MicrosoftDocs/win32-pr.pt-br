---
description: A estrutura PID MAP contém identifica o conteúdo de uma ID de pacote de fluxo de transporte \_ MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: PID_MAP (Bdatypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 1e5712c9fd18e7503d477908886868784e7dc7a9f4ced7e77ab54b7d7dc71d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119302786"
---
# <a name="pid_map-structure"></a>Estrutura PID \_ MAP

A estrutura contém identifica o conteúdo de uma ID de pacote de fluxo de transporte `PID_MAP` MPEG-2.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Membros

<dl> <dt>

**ulPID**
</dt> <dd>

Especifica a ID do pacote (PID)

</dd> <dt>

**MediaSampleContent**
</dt> <dd>

Especifica o conteúdo do conteúdo do pacote, como um tipo de [**enumeração MEDIA \_ SAMPLE \_ CONTENT.**](media-sample-content.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Bdatypes.h (inclua Bdaiface.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Estruturas](directshow-structures.md)
</dt> <dt>

[**IEnumPIDMap Interface**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




