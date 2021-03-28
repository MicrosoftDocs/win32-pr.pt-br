---
description: Este tópico lista os construtores da classe Font. Para obter uma listagem de classe completa, consulte classe Font.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Construtores de fonte. Font
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: bdf533e292734956c02d3f8a424ca619cb722c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171733"
---
# <a name="fontfont-constructors"></a>Construtores de fonte. Font

Este tópico lista os construtores da classe [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Para obter uma listagem de classe completa, consulte **classe Font**.

### <a name="overload-list"></a>Lista de sobrecargas



| Construtor                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fonte (HDC, HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Cria um objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) indiretamente de uma fonte lógica GDI usando um identificador para uma estrutura de **LOGFONT** GDI.<br/>                                                                                                                                   |
| [**Fonte (HDC, LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Cria um objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) diretamente de uma fonte lógica GDI. A fonte lógica GDI é uma estrutura **LOGFONTA** , que é a versão de caractere de um byte de uma fonte lógica. Esse construtor é fornecido para compatibilidade com GDI.<br/> |
| [**Fonte (HDC, LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Cria um objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) diretamente de uma fonte lógica GDI. A fonte lógica GDI é uma estrutura **LOGFONTW** , que é a versão de caractere largo de uma fonte lógica. Esse construtor é fornecido para compatibilidade com GDI.<br/>     |
| [**Fonte (FontFamily \* , real, int, unidade)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Cria um objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) com base em um objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , um tamanho, um estilo de fonte e uma unidade de medida.<br/>                                                                               |
| [**Fonte (WCHAR \* , real, int, unidade, fontecollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Cria um objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) com base em uma família de fontes, um tamanho, um estilo de fonte, uma unidade de medida e um objeto [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .<br/>                                     |
| [**Fonte (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Cria um objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) com base no objeto de fonte GDI selecionado no momento em um contexto de dispositivo especificado. Esse construtor é fornecido para compatibilidade com GDI. <br/>                                                                           |



 

 
