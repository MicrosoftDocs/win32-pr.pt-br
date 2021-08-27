---
title: Copiar quadros individuais de uma imagem de vários quadros
description: O exemplo a seguir recupera os quadros individuais de um arquivo TIFF de vários quadros.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398df806ad56b65114b0cc9a986ea53061183fa4658872b65b7d08ef7e38a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115096"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Copiar quadros individuais de uma imagem de vários quadros

O exemplo a seguir recupera os quadros individuais de um arquivo TIFF de vários quadros. Quando o arquivo TIFF foi criado, os quadros individuais foram adicionados à dimensão Página (consulte Criando e [salvando uma Multiple-Frame imagem](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). O código exibe cada uma das quatro páginas e salva cada página em um arquivo de disco PNG separado.

O código constrói um [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo TIFF de vários quadros. Para recuperar os quadros individuais (páginas), o código chama o [**método Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) desse **objeto Image.** O primeiro argumento passado para o método **Image::SelectActiveFrame** é o endereço de um GUID que especifica a dimensão na qual os quadros foram adicionados anteriormente ao arquivo TIFF de vários quadros. O GUID FrameDimensionPage é definido em Gdiplusimaging.h. Outros GUIDs definidos nesse arquivo de header são FrameDimensionTime e FrameDimensionResolution. O segundo argumento passado para **o método Image::SelectActiveFrame** é o índice baseado em zero da página desejada.

O código se baseia na função auxiliar GetEncoderClsid, que é mostrada em Recuperando o Identificador de Classe para [um Codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



A ilustração a seguir mostra as páginas individuais, conforme exibido pelo código anterior.

![ilustração mostrando uma forma geométrica, uma foto de cor, uma foto monocromática e uma forma geométrica diferente](images/multiframe1.png)

 

 



