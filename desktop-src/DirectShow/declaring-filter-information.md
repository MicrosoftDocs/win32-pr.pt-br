---
description: Declarando informações de filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Declarando informações de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646127"
---
# <a name="declaring-filter-information"></a>Declarando informações de filtro

A primeira etapa é declarar as informações de filtro, se necessário. O DirectShow define as seguintes estruturas para descrever filtros, pins e tipos de mídia:



| Estrutura                                               | Descrição             |
|---------------------------------------------------------|-------------------------|
| [**filtro de AMOVIESETUP \_**](amoviesetup-filter.md)       | Descreve um filtro.     |
| [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md)             | Descreve um PIN.        |
| [**\_MediaType AMOVIESETUP**](amoviesetup-mediatype.md) | Descreve um tipo de mídia. |



 

Essas estruturas são aninhadas. A estrutura do **\_ filtro AMOVEIESETUP** tem um ponteiro para uma matriz de estruturas de **\_ PIN AMOVIESETUP** , e cada uma delas tem um ponteiro para uma matriz de estruturas **AMOVEIESETUP \_ MediaType** . Juntas, essas estruturas fornecem informações suficientes para a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) localizar um filtro. Elas não são uma descrição completa de um filtro. Por exemplo, se o filtro criar várias instâncias do mesmo PIN, você deverá declarar apenas uma estrutura [**de \_ PIN AMOVIESETUP**](amoviesetup-pin.md) para esse PIN. Além disso, um filtro não é necessário para dar suporte a todas as combinações de tipos de mídia que ele registra; Nem é necessário registrar todos os tipos de mídia aos quais ele dá suporte.

Declare as estruturas de configuração como variáveis globais dentro de sua DLL. O exemplo a seguir mostra um filtro com um pino de saída:


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



O nome do filtro é declarado como uma variável global estática, pois ele será usado novamente em outro lugar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como registrar filtros do DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



