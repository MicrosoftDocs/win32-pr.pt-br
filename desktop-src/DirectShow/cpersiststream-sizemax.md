---
description: Recupera o tamanho máximo de bytes necessário para o fluxo atual, não incluindo o número de versão.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Método CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771843"
---
# <a name="cpersiststreamsizemax-method"></a>Método CPersistStream. SizeMax

Recupera o tamanho máximo de bytes necessário para o fluxo atual, não incluindo o número de versão.

## <a name="syntax"></a>Sintaxe


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o número de bytes necessários para os dados, não incluindo o número de versão.

## <a name="remarks"></a>Comentários

A versão padrão retorna zero; Ele deve ser substituído para fornecer algum outro valor apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




