---
title: Alterando predefinições
description: Alterando predefinições
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizações, exemplo de brilho
- visualizações personalizadas, exemplo de brilho
- Guia de programação, visualizações
- amostras, visualização de brilho
- Exemplo de visualização de brilho
- visualizações, predefinições
- visualizações personalizadas, predefinições
- predefinições em visualizações, exemplo de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759735"
---
# <a name="changing-presets"></a>Alterando predefinições

As seções de código predefinida a seguir foram alteradas para permitir três predefinições:

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

A seguinte enumeração em brilho. h foi alterada para permitir três predefinições:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Cabeçalho do recurso

Os recursos a seguir foram definidos em Resource. h para permitir três predefinições:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Observe que você também deve alterar o número do recurso do **\_ APS \_ próximo \_ \_ valor SYMED** para 106.

## <a name="resource-file"></a>Arquivo de recurso

As cadeias de caracteres a seguir devem ser alteradas no arquivo Glowdll. rc para permitir três predefinições e dar a eles nomes:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de brilho**](the-glow-sample.md)
</dt> </dl>

 

 




