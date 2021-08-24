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
ms.openlocfilehash: 0ca5832246e90e1df207754dc33380547b8193829394d81e6b2b757fccf79a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502306"
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
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 




