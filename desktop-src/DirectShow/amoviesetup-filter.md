---
description: A \_ estrutura do filtro AMOVIESETUP contém informações para registrar um filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Estrutura de AMOVIESETUP_FILTER (combase. h)
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
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747425"
---
# <a name="amoviesetup_filter-structure"></a>\_Estrutura do filtro AMOVIESETUP

A estrutura do **\_ filtro AMOVIESETUP** contém informações para registrar um filtro.

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

**clsID**
</dt> <dd>

Identificador de classe do filtro.

</dd> <dt>

**strName**
</dt> <dd>

Nome do filtro.

</dd> <dt>

**dwMerit**
</dt> <dd>

Mérito de filtro. Usado pela interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) ao construir um grafo de filtro. Para obter uma lista de valores de mérito, consulte [mérito](merit.md).

</dd> <dt>

**nPins**
</dt> <dd>

Número de elementos na matriz *lpPin* . Se *lpPin* for **nulo**, defina esse membro como zero.

</dd> <dt>

**lpPin**
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**\_ PIN AMOVIESETUP**](amoviesetup-pin.md) , de tamanho *nPins*. Cada membro desta matriz descreve um PIN no filtro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter informações sobre como usar essa estrutura, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md). Use essa estrutura somente para filtros registrados na categoria de filtro padrão (CLSID \_ LegacyAmFilterCategory). Para registrar um filtro em uma categoria diferente, use o método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , conforme descrito em [implementando DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> O arquivo de cabeçalho combase. h é fornecido com as [classes base do DirectShow](directshow-base-classes.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do DirectShow](directshow-structures.md)
</dt> </dl>

 

 




