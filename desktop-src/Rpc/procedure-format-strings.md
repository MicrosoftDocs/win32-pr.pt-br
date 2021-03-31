---
title: Cadeias de caracteres de formato de procedimento
description: A seguir está uma descrição completa da cadeia de caracteres de formato. Ele monta todas as camadas relacionadas a diferentes estágios da evolução do intérprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917539"
---
# <a name="procedure-format-strings"></a>Cadeias de caracteres de formato de procedimento

A seguir está uma descrição completa da cadeia de caracteres de formato. Ele monta todas as camadas relacionadas a diferentes estágios da evolução do intérprete.

## <a name="procedure-descriptor-overview"></a>Visão geral do descritor de procedimento

Um descritor de procedimento consiste nos descritores de cabeçalho e nos descritores de parâmetro. A descrição do estilo [**– Oi**](/windows/desktop/Midl/-oi) é considerada desatualizada, em termos de uso comum na programação de RPC atual. O **– OIF** é considerado mais atual.

## <a name="the-oi-style-description"></a>A descrição do estilo – Oi

Essa descrição consiste no seguinte:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

O cabeçalho teria de 6 a 16 bytes.

A descrição completa é gerada durante a compilação no modo [**– Oi**](/windows/desktop/Midl/-oi) . No [**– modo do sistema operacional**](/windows/desktop/Midl/-os) , somente os descritores de parâmetro são gerados, que são usados para conversão. O intérprete de seleção usa descritores de parâmetro de estilo antigo.

## <a name="the-oif-style-description"></a>A descrição do estilo – OIF

A descrição consiste no seguinte:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

O descritor do cabeçalho de estilo [**– OIF**](/windows/desktop/Midl/-oi) consiste em

A descrição do estilo – OIF é gerada durante a compilação no modo [**– OIF**](/windows/desktop/Midl/-oi) ou **– Oicf** do compilador.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Alguns recursos mais recentes, como pipe, Async e [**/robust**](/windows/desktop/Midl/-robust) , forçam o modo [**– Oicf**](/windows/desktop/Midl/-oi) do compilador, quando usado.

## <a name="the-extended-oif-description"></a>A descrição estendida – OIF

A descrição consiste no seguinte:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 