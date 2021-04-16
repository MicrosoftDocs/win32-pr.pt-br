---
description: Método de construtor.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Construtor CBaseAllocator. CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750910"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Construtor CBaseAllocator. CBaseAllocator

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome de depuração do alocador. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Defina o valor como S \_ OK antes de criar o objeto. Se o Construtor falhar, o valor será definido como um código de erro.

</dd> <dt>

*beventilação* 
</dt> <dd>

Valor booliano que indica se um semáforo deve ser criado. Se **for true**, o alocador criará um semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)), que é sinalizado sempre que um exemplo se tornar disponível. Defina o valor como **false** se você estiver implementando uma classe derivada que não requer um semáforo.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Valor booliano que indica se o mecanismo de retorno de chamada da versão está habilitado. Defina o valor como **true** se desejar fornecer uma interface de retorno de chamada, que é chamada quando os buffers são liberados. Especifique o retorno de chamada chamando o método [**CBaseAllocator:: Setnotificar**](cbaseallocator-setnotify.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




