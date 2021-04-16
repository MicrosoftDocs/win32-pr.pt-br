---
description: Identificador para a instância do módulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Membro CBaseWindow:: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751254"
---
# <a name="cbasewindowm_hinstance-member"></a>Membro de CBaseWindow:: m \_ HINSTANCE

Identificador para a instância do módulo.

## <a name="syntax"></a>Sintaxe


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Comentários

A função de ponto de entrada de DLL define uma variável global com um identificador para a instância do módulo. A classe **CBaseWindow** armazena esse identificador em seu método construtor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




