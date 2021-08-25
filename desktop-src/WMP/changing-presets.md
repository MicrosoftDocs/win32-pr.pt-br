---
title: Alterando predefinições
description: Alterando predefinições
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizações, exemplo de Brilho
- visualizações personalizadas, amostra de Brilho
- guia de programação, visualizações
- exemplos, visualização do Brilho
- Exemplo de visualização de brilho
- visualizações, predefinições
- visualizações personalizadas, predefinições
- predefinições em visualizações, amostra de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03828614093836c5f9a3b422167b62f11b8f2489eb30556d42a2d80495935ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863906"
---
# <a name="changing-presets"></a>Alterando predefinições

As seções de código predefinidas a seguir foram alteradas para permitir três predefinições:

## <a name="getpresettitle"></a>GetPresetTitle

Esse código foi inserido no lugar do código predefinido gerado:


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>Enumerações

A enumeração a seguir em Brilho.h foi alterada para permitir três predefinições:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Header de recurso

Os seguintes recursos foram definidos em Resource.h para permitir três predefinições:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Observe que você também deve alterar o número de recursos **\_ APS NEXT \_ \_ SYMED \_ VALUE** para 106.

## <a name="resource-file"></a>Arquivo de recurso

As seguintes cadeias de caracteres devem ser alteradas no arquivo Brilhodll.rc para permitir três predefinições e dar a eles nomes:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de brilho**](the-glow-sample.md)
</dt> </dl>

 

 




