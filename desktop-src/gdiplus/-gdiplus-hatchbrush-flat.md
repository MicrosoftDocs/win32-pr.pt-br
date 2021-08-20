---
description: Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe HatchBrush C++.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Funções Do HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f550f3f3567a5835c7a220d0384dc1c6bbd24133577b9b89a6a37a0aae8840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067010"
---
# <a name="hatchbrush-functions"></a>Funções Do HatchBrush

Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat.h. As funções no GDI+ API simples são envolvidas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que fizer chamadas para GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++. Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos wrapper, [consulte GDI+ API Simples.](-gdiplus-flatapi-flat.md)

As funções de API simples a seguir são empacotadas pela [**classe HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) C++.

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Funções HatchBrush e métodos wrapper correspondentes



| Função simples                                                                                                               | Método Wrapper                                                                                                                                                                                   | Comentários                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush(GpHatchStyle hatchstyle, ARGB forecol, ARGB backcol, pincel \* \* gpHatch)<br/> | [**HatchBrush::HatchBrush(IN HatchStyle hatchStyle, IN const Color& foreColor, IN const Color& backColor = Color())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Cria um [**objeto HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) com base em um estilo de hatch, uma cor de primeiro plano e uma cor da tela de fundo. |
| GpStatus WINGDIPAPI GdipGetHatchStyle (pincel gpHatch, \* \* ha hatchstyle gpHatchStyle)<br/>                                | [**HatchStyle HatchBrush::GetHatchStyle() const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Obtém o estilo de hatch deste pincel de hatch.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor(pincel gpHatch, \* \* forecol ARGB)<br/>                                 | [**Status HatchBrush::GetForegroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Obtém a cor de primeiro plano desse pincel de hatch.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor(pincel gpHatch, \* \* backcol ARGB)<br/>                                 | [**Status HatchBrush::GetBackgroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Obtém a cor da tela de fundo desse pincel de hatch.                                                                                             |



 

 

 
