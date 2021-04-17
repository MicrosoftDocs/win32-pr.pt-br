---
description: Ponteiro para o alocador que criou este exemplo.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Membro CMediaSample:: m_pAllocator (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769228"
---
# <a name="cmediasamplem_pallocator-member"></a>Membro de CMediaSample:: m \_ pAllocator

Ponteiro para o alocador que criou este exemplo.

## <a name="syntax"></a>Sintaxe


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Comentários

Embora o exemplo mantenha um ponteiro para o alocador, ele não mantém uma contagem de referência. Em vez disso, o alocador incrementa sua própria contagem de referência no método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) e se libera no método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) . Isso garante que o alocador estará disponível desde que outro objeto esteja usando o exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




