---
description: O método PreparePalette configura uma paleta, com base em um tipo de mídia do filtro proprietário.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Método CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758855"
---
# <a name="cimagepalettepreparepalette-method"></a>Método CImagePalette. PreparePalette

O `PreparePalette` método configura uma paleta, com base em um tipo de mídia do filtro proprietário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pmtNew* 
</dt> <dd>

Ponteiro para o novo tipo de mídia. O bloco de formato deve ser uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> <dt>

*pmtOld* 
</dt> <dd>

Ponteiro para o tipo de mídia antigo. Se o tipo de mídia estiver sendo definido pela primeira vez, esse parâmetro poderá ser um tipo vazio sem nenhum bloco de formato. Caso contrário, o bloco de formato deve ser uma estrutura **VIDEOINFOHEADER** .

</dd> <dt>

*szDevice* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI. Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se a paleta tiver sido atualizada ou S \_ false se a paleta não foi alterada.

## <a name="remarks"></a>Comentários

Se a paleta precisar ser atualizada, esse método executará as seguintes ações:

-   Chama [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) para criar uma nova paleta lógica.
-   Envia um evento de [**\_ \_ alteração de paleta do EC**](ec-palette-changed.md) para o Gerenciador do grafo de filtro.
-   Chama [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) no objeto **CBaseWindow** .
-   Chama [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) no objeto **CDrawImage** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




