---
description: Um segmento de reconhecimento é a unidade de tinta básica que um reconhecedor usa internamente para produzir um resultado de reconhecimento para um objeto de tinta específico.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmentos de reconhecimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768215"
---
# <a name="recognition-segments"></a>Segmentos de reconhecimento

Um segmento de reconhecimento é a unidade de tinta básica que um reconhecedor usa internamente para produzir um resultado de reconhecimento para um objeto de tinta específico. Um segmento de reconhecimento é uma coleção de traços de tinta. Por exemplo, um reconhecedor capaz de reconhecer manuscritos cursivos em inglês pode usar uma palavra como o segmento de reconhecimento básico.

Outros reconhecedores podem usar partes de palavras compostas como segmentos básicos. Por exemplo, em espanhol, as palavras curtas são normalmente combinadas para fornecer palavras compostas mais longas. "Damelo" é uma palavra em espanhol que é composta por três palavras "da minha mão" (Dê-me isso), mas é escrito como uma única palavra. Um reconhecedor de espanhol poderia reconhecer cada subpalavra como um segmento.

Um reconhecedor pode encontrar várias maneiras de dividir uma amostra de tinta em segmentos de reconhecimento. Como a ambiguidade está envolvida no reconhecimento da entrada pretendida do usuário, o reconhecedor pode retornar muitas correspondências alternativas.

Para obter mais informações sobre alternativas, consulte [alternativas](alternates.md).

 

 



