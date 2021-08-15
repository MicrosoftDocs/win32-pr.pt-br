---
description: Este tópico lista os construtores da classe Font. Para uma listagem de classe completa, consulte Classe font.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Construtores Font.Font
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ff876120655adcf58318a471ed66ddfa4502d625305d9fda37f01c966e19e0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977896"
---
# <a name="fontfont-constructors"></a>Construtores Font.Font

Este tópico lista os construtores da [**classe Font.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Para uma listagem de classe completa, consulte **Classe font**.

### <a name="overload-list"></a>Lista de sobrecargas



| Construtor                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Font(HDC,HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Cria um [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) indiretamente de uma fonte lógica GDI usando um identificador para uma estrutura **GDI LOGFONT.**<br/>                                                                                                                                   |
| [**Font(HDC,LOG GAZETA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Cria um [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) diretamente de uma fonte lógica GDI. A fonte lógica GDI é uma **estrutura LOG GAZETA,** que é a versão de caractere de um byte de uma fonte lógica. Esse construtor é fornecido para compatibilidade com gDI.<br/> |
| [**Font(HDC,LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Cria um [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) diretamente de uma fonte lógica GDI. A fonte lógica GDI é uma **estrutura LOGFONTW,** que é a versão de caractere largo de uma fonte lógica. Esse construtor é fornecido para compatibilidade com gDI.<br/>     |
| [**Font(FontFamily,REAL, \* INT,Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Cria um [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) com base em um objeto [**FontFamily,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) um tamanho, um estilo de fonte e uma unidade de medida.<br/>                                                                               |
| [**Font(WCHAR, \* REAL, INT, Unit,FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Cria um [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) com base em uma família de fontes, um tamanho, um estilo de fonte, uma unidade de medida e um [**objeto FontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)<br/>                                     |
| [**Font(HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Cria um [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) com base no objeto de fonte GDI selecionado atualmente em um contexto de dispositivo especificado. Esse construtor é fornecido para compatibilidade com gDI. <br/>                                                                           |



 

 
