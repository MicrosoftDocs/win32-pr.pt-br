---
description: A \_ estrutura do mapa PID contém identifica o conteúdo de uma ID de pacote de fluxo de transporte MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Estrutura de PID_MAP (Bdatypes. h)
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
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782838"
---
# <a name="pid_map-structure"></a>\_Estrutura do mapa PID

A `PID_MAP` estrutura contém identifica o conteúdo de uma ID de pacote de fluxo de transporte MPEG-2.

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

Especifica o conteúdo da carga do pacote, como um tipo de enumeração de [**\_ \_ conteúdo de exemplo de mídia**](media-sample-content.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Bdatypes. h (incluir Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do DirectShow](directshow-structures.md)
</dt> <dt>

[**Interface IEnumPIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




