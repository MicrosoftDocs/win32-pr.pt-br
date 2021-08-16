---
description: A estrutura AMOVIESETUP \_ FILTER contém informações para registrar um filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: AMOVIESETUP_FILTER (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: fe50295f87e2932d3eb0fe53aac4896343a31441f8fa832bbaa69d5256846414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824786"
---
# <a name="amoviesetup_filter-structure"></a>Estrutura AMOVIESETUP \_ FILTER

A **estrutura AMOVIESETUP \_ FILTER** contém informações para registrar um filtro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Clsid**
</dt> <dd>

Identificador de classe do filtro.

</dd> <dt>

**strName**
</dt> <dd>

Nome do filtro.

</dd> <dt>

**dwMerit**
</dt> <dd>

Filtrar o sr. Usado pela interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) ao construir um grafo de filtro. Para ver uma lista de valores de valores de valor, consulte [Também.](merit.md)

</dd> <dt>

**nPins**
</dt> <dd>

Número de elementos na matriz *lpPin.* Se *lpPin* for **NULL,** define esse membro como zero.

</dd> <dt>

**lpPin**
</dt> <dd>

Ponteiro para uma matriz de estruturas [**\_ DE PIN AMOVIESETUP,**](amoviesetup-pin.md) de *tamanho nPins*. Cada membro dessa matriz descreve um pin no filtro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter informações sobre como usar essa estrutura, [consulte How to Register DirectShow Filters](how-to-register-directshow-filters.md). Use essa estrutura somente para filtros registrados na categoria de filtro padrão (CLSID \_ LegacyAmFilterCategory). Para registrar um filtro em uma categoria diferente, use o método [**IFilterMapper2::RegisterFilter,**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) conforme descrito em [Implementando DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> O arquivo de header combase.h é fornecido com o [DirectShow Classes Base](directshow-base-classes.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Estruturas](directshow-structures.md)
</dt> </dl>

 

 




