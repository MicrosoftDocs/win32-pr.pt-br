---
description: Construtor de CImageAllocator. CImageAllocator-método de construtor.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Construtor CImageAllocator. CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71d7ca547556c151107c35c9ece1f4ee0d0ca6a80feb6db0cebb06878ddbca01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131216"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>Construtor CImageAllocator. CImageAllocator

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro proprietário.

</dd> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome de depuração do alocador. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Defina o valor como S \_ OK antes de criar o objeto. Se o Construtor falhar, o valor será definido como um código de erro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




