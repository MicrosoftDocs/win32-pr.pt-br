---
description: Os seguintes identificadores globalmente exclusivos (GUIDs) são usados pelo diário do Windows para identificar Propriedades personalizadas em traçados ou atributos de desenho.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUIDs de propriedade personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790465"
---
# <a name="custom-property-guids"></a>GUIDs de propriedade personalizada

Os seguintes identificadores globalmente exclusivos (GUIDs) são usados pelo diário do Windows para identificar Propriedades personalizadas em traçados ou atributos de desenho.

## <a name="guid_stroke_timestamp"></a>\_carimbo de \_ data/hora de traço GUID


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



Essa é uma estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) que indica a hora em que o traço foi criado ou adicionado ao documento.


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>\_hora de corte do GUID \_


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



Esta é uma estrutura de **TimeID** . Ele permite que a ordem dos traços seja mantida nas operações de colar e soltar. Sem a estrutura de **TimeID** , o carimbo de data/hora para todos os objetos da [**interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recortados e colados em uma [coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) será o mesmo.


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>realce de GUID \_

É um **bool**, em que **true**= Ink do realçador, **false**= Ink regular. Isso é aplicado aos atributos de desenho.


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>estilo de tinta de GUID em \_ \_ \_ negrito

É um **bool**, onde **true**= Ink negrito, **false**= normal. Isso é aplicado aos atributos de desenho.


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>\_itálico do \_ estilo de tinta do GUID \_

É um **bool**, onde **true**= Ink em itálico, **false**= normal. Isso é aplicado aos atributos de desenho.


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IJournalReader**](ijournalreader.md)
</dt> </dl>

 

 
