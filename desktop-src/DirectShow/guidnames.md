---
description: GuidNames é uma matriz global na biblioteca de classes base do DirectShow que contém cadeias de caracteres que representam os GUIDs definidos em UUIDs. h. Essa matriz é útil para gerar a saída de depuração.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778479"
---
# <a name="guidnames"></a>GuidNames

`GuidNames` é uma matriz global na biblioteca de classes base do DirectShow que contém cadeias de caracteres que representam os GUIDs definidos em UUIDs. h. Essa matriz é útil para gerar a saída de depuração.

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*volume*
</dt> <dd>

Especifica qualquer valor de GUID definido no arquivo de cabeçalho UUIDs. h.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use essa matriz global para gerar constantes de GUID como cadeias de caracteres. Por exemplo, o código a seguir imprime a cadeia de caracteres " \_ vídeo de MediaType" no console:


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



Se o GUID não for correspondido, a cadeia de caracteres "nome de GUID desconhecido" será retornada. Nem todos os GUIDs do DirectShow são definidos em UUIDs. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




