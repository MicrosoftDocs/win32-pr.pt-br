---
description: O método SetStretchMode calcula se a imagem de vídeo deve ser alongada.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Método CDrawImage.SetStretchMode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3886910bce57aca728f64ffbe9d660c1073d1281864a7721faa7e757c7c7d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526486"
---
# <a name="cdrawimagesetstretchmode-method"></a>Método CDrawImage.SetStretchMode

O `SetStretchMode` método calcula se a imagem de vídeo deve ser alongada.

## <a name="syntax"></a>Sintaxe


```C++
void SetStretchMode();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A **classe CDrawImage chama** automaticamente esse método sempre que o retângulo de origem ou de destino muda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




