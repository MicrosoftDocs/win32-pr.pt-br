---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Funções HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d444fea500ce1e56e4c59420b913d5ff6cee965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988868"
---
# <a name="hatchbrush-functions"></a>Funções HatchBrush

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

As funções de API simples a seguir são encapsuladas pela classe [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) C++.

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Funções HatchBrush e métodos wrapper correspondentes



| Função Flat                                                                                                               | Método de wrapper                                                                                                                                                                                   | Comentários                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush (GpHatchStyle HatchStyle, ARGB forecol, ARGB backcol, pincel de GpHatch \* \* )<br/> | [**HatchBrush:: HatchBrush (em HatchStyle hatchStyle, na cor const& foreColor, na cor const& backColor = Color ())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Cria um objeto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) com base em um estilo de hachura, uma cor de primeiro plano e uma cor de plano de fundo. |
| GpStatus WINGDIPAPI GdipGetHatchStyle (GpHatch \* Brush, GpHatchStyle \* HatchStyle)<br/>                                | [**HatchStyle HatchBrush:: gethachurastyle () const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Obtém o estilo de hachura deste pincel de hachura.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor (GpHatch \* Brush, \* forecol ARGB)<br/>                                 | [**HatchBrush de status:: GetForegroundColor (cor de cor de saída \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Obtém a cor de primeiro plano deste pincel de hachura.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor (GpHatch \* Brush, \* backcol ARGB)<br/>                                 | [**Status HatchBrush:: getBackgroundColor (cor de cor de saída \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Obtém a cor do plano de fundo deste pincel de hachura.                                                                                             |



 

 

 
