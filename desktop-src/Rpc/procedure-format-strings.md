---
title: Cadeias de caracteres de formato de procedimento
description: A seguir está uma descrição completa da cadeia de caracteres de formato. Ele monta todas as camadas relacionadas a diferentes estágios da evolução do interpretador.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb17434a1c05b66212283237d61ee4492aa23ed0bf1ecca75f1fec1b3ddd784b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019054"
---
# <a name="procedure-format-strings"></a>Cadeias de caracteres de formato de procedimento

A seguir está uma descrição completa da cadeia de caracteres de formato. Ele monta todas as camadas relacionadas a diferentes estágios da evolução do interpretador.

## <a name="procedure-descriptor-overview"></a>Visão geral do descritor de procedimento

Um descritor de procedimento consiste nos descritores de header e nos descritores de parâmetro. A [**descrição de estilo –Oi**](/windows/desktop/Midl/-oi) é considerada desatualizada, em termos de uso comum na programação RPC atual. O **–Oif** é considerado mais atual.

## <a name="the-oi-style-description"></a>A descrição do estilo –Oi

Essa descrição consiste no seguinte:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

O header teria de 6 a 16 bytes.

A descrição completa é gerada durante a compilação [**no modo –Oi.**](/windows/desktop/Midl/-oi) No [**modo –Os,**](/windows/desktop/Midl/-os) somente os descritores de parâmetro são gerados, que são usados para conversão. O interpretador de seleções usa descritores de parâmetro de estilo antigo.

## <a name="the-oif-style-description"></a>A descrição do estilo –Oif

A descrição consiste no seguinte:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

O descritor de cabeça de estilo [**–Oif**](/windows/desktop/Midl/-oi) consiste em

A descrição de estilo –Oif é gerada durante a compilação no [**modo –Oif**](/windows/desktop/Midl/-oi) ou **–Oicf** do compilador.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Alguns recursos mais recentes, como pipe, assíncrono e [**/robust,**](/windows/desktop/Midl/-robust) forçam o [**modo –Oicf**](/windows/desktop/Midl/-oi) do compilador, quando usados.

## <a name="the-extended-oif-description"></a>A descrição estendida –Oif

A descrição consiste no seguinte:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 