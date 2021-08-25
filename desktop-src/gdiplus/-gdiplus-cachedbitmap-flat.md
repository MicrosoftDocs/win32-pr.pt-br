---
description: Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe C++ CachedBitmap.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Funções CachedBitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1835cd668df90a7703a4aebdd60d37d877fe571f376d440080f5668ec3926a26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888326"
---
# <a name="cachedbitmap-functions"></a>Funções CachedBitmap

Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h. As funções na API GDI+ simples são empacotadas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que fizer chamadas para GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++. Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, [consulte GDI+ API Simples.](-gdiplus-flatapi-flat.md)

As funções de API simples a seguir são empacotadas pela [**classe C++ CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Funções CachedBitmap e métodos wrapper correspondentes



| Função simples                                                                                                             | Método Wrapper                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap( \* Bitmap gpBitmap, \* gráficos GpGraphics, GpCachedBitmap \* \* cachedBitmap )   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Cria um [**objeto CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) com base em um [**objeto Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e um [**objeto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) O bitmap armazenado em cache pega os dados de pixel do objeto **Bitmap** e os armazena em um formato otimizado para o dispositivo de exibição associado ao **objeto Graphics.** |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap(GpCachedBitmap \* cachedBitmap)<br/>                                      | ~CachedBitmap()                                                                                 | Limpa os recursos usados por um [**objeto CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap( \* GpGraphics graphics, GpCachedBitmap \* cachedBitmap, INT x, INT y )            | [**Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | O [**método Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) desenha a imagem armazenada em um [**objeto CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits( HEN LTDAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags )<br/> | [**Metafile::EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Converte um metarquivo de formato aprimorado em um metarquivo WMF (formato de metarquivo de Windows) e armazena os registros convertidos em um buffer especificado.                                                                                                                                                                                                                                                                                       |



 

 

