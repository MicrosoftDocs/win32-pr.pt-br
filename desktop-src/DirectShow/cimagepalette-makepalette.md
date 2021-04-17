---
description: O método MakePalette cria uma paleta lógica da tabela de cores em um formato de vídeo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Método CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789712"
---
# <a name="cimagepalettemakepalette-method"></a>Método CImagePalette. MakePalette

O `MakePalette` método cria uma paleta lógica da tabela de cores em um formato de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém a tabela de cores.

</dd> <dt>

*szDevice* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI. Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, retorna um identificador para a paleta. Caso contrário, retornará **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




