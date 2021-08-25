---
description: Recupera o tamanho máximo de byte necessário para o fluxo atual, não incluindo o número de versão.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Método CPersistStream.SizeMax (Pstream.h)
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
ms.openlocfilehash: 2b8f2c547e75303e4c54a49651f2118a90768bc0f42161ee3dae0de9bec2dcad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813296"
---
# <a name="cpersiststreamsizemax-method"></a>Método CPersistStream.SizeMax

Recupera o tamanho máximo de byte necessário para o fluxo atual, não incluindo o número de versão.

## <a name="syntax"></a>Sintaxe


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o número de bytes necessários para os dados, não incluindo o número de versão.

## <a name="remarks"></a>Comentários

A versão padrão retorna zero; ele deve ser substituído para fornecer algum outro valor apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




