---
description: A função LoadOLEAut32 carrega a biblioteca de vínculo dinâmico de automação (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Função LoadOLEAut32 (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812976"
---
# <a name="loadoleaut32-function"></a>Função LoadOLEAut32

A função **LoadOLEAut32** carrega a biblioteca de vínculo dinâmico de automação (OleAut32.dll).

## <a name="syntax"></a>Sintaxe


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um identificador para uma instância de DLL de automação.

## <a name="remarks"></a>Comentários

Quando o destruidor [**CBaseObject**](cbaseobject.md) destrói o objeto que carregou OleAut32.dll, ele descarregará a biblioteca se ainda estiver carregada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 




