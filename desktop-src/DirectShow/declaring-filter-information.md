---
description: Declarando informações de filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Declarando informações de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c22fb13b524bed56e8cc9d51e573f2729f843e56565db2793d1a8b4568af52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953195"
---
# <a name="declaring-filter-information"></a>Declarando informações de filtro

A primeira etapa é declarar as informações de filtro, se necessário. DirectShow define as seguintes estruturas para descrever filtros, pinos e tipos de mídia:



| Estrutura                                               | Descrição             |
|---------------------------------------------------------|-------------------------|
| [**FILTRO \_ AMOVIESETUP**](amoviesetup-filter.md)       | Descreve um filtro.     |
| [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md)             | Descreve um pin.        |
| [**AMOVIESETUP \_ MEDIATYPE**](amoviesetup-mediatype.md) | Descreve um tipo de mídia. |



 

Essas estruturas são aninhadas. A **estrutura AMOVEIESETUP \_ FILTER** tem um ponteiro para uma matriz de estruturas DE **\_ PIN AMOVIESETUP** e cada uma delas tem um ponteiro para uma matriz de estruturas **AMOVEIESETUP \_ MEDIATYPE.** Juntas, essas estruturas fornecem informações suficientes para a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) localizar um filtro. Eles não são uma descrição completa de um filtro. Por exemplo, se o filtro criar várias instâncias do mesmo pin, você deverá declarar apenas uma estrutura [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md) para esse pino. Além disso, um filtro não é necessário para dar suporte a todas as combinações de tipos de mídia que ele registra; nem é necessário para registrar todos os tipos de mídia com suporte.

Declare as estruturas de configuração como variáveis globais em sua DLL. O exemplo a seguir mostra um filtro com um pino de saída:


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



O nome do filtro é declarado como uma variável global estática, porque ele será usado novamente em outro lugar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como registrar filtros DirectShow dados](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



