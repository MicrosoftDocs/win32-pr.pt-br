---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Funções CachedBitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebb19648e38425561d1a1609c5f71368718ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661947"
---
# <a name="cachedbitmap-functions"></a>Funções CachedBitmap

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

As funções de API simples a seguir são encapsuladas pela classe [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) C++.

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Funções CachedBitmap e métodos wrapper correspondentes



| Função Flat                                                                                                             | Método de wrapper                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap (GpBitmap \* bitmap, GpGraphics \* Graphics, GpCachedBitmap \* \* cachedBitmap)   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Cria um objeto [**CachedBitmap:: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) com base em um objeto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . O bitmap armazenado em cache usa os dados de pixel do objeto **bitmap** e os armazena em um formato que é otimizado para o dispositivo de vídeo associado ao objeto **Graphics** . |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap (GpCachedBitmap \* cachedBitmap)<br/>                                      | ~ CachedBitmap ()                                                                                 | Limpa os recursos usados por um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap (GpGraphics \* Graphics, GpCachedBitmap \* CACHEDBITMAP, int x, int y)            | [**Gráficos::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | O método [**Graphics::D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) desenha a imagem armazenada em um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits (HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapmode, INT eFlags)<br/> | [**Metarquivo:: EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Converte um metarquivo de formato avançado em um metarquivo formato WMF (WMF) e armazena os registros convertidos em um buffer especificado.                                                                                                                                                                                                                                                                                       |



 

 

