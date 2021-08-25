---
description: Essa classe é a classe de tipo de evento para eventos de alocação virtual. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: fa3dd8eb53e9c1a79cf38edde0d9c4dba93ea85b0994bfb316b97064f211f26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927566"
---
# <a name="pagefault_virtualalloc-class"></a>Classe PageFault \_ VirtualAlloc

Essa classe é a classe de tipo de evento para eventos de alocação virtual.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a>Membros

A **classe PageFault \_ VirtualAlloc** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe PageFault \_ VirtualAlloc** tem essas propriedades.

<dl> <dt>

**Baseaddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Pointer
</dt> </dl>

O endereço inicial no qual a memória foi alocada ou liberada.

</dd> <dt>

**Sinalizadores**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4), Format("x")
</dt> </dl>

O tipo de alocação de memória que foi executada. Para valores possíveis, consulte *o parâmetro flAllocationType* da [**função VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

O processo que possui a memória (pode ser diferente do thread que realizou a alocação).

</dd> <dt>

**RegionSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), Extension("SizeT")
</dt> </dl>

O tamanho, em bytes, da memória que foi alocada ou liberada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 
