---
description: Uma alternativa é uma correspondência de palavra potencial para um segmento de reconhecimento. Um reconhecedor gera alternativas e as baseia em correspondências aceitáveis da entrada de tinta ou áudio em um dicionário ou um factor.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76faf27b82a6bfc064fddbad3d2d4ca6c2dddc098d56bca340b677cea17a319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119337036"
---
# <a name="alternates"></a>Alternativos

Uma alternativa é uma correspondência de palavra potencial para um segmento de reconhecimento. Um reconhecedor gera alternativas e as baseia em correspondências aceitáveis da entrada de tinta ou áudio em um dicionário ou um factor.

> [!Note]  
> Atualmente, a avaliação de confiança está disponível apenas para os reconhecedores de gestos (Estados Unidos) e em inglês da Microsoft.

 

Às vezes, a tinta pode ter distinções ambíguas entre segmentos. O reconhecedor compara esses segmentos com um dicionário do reconhecedor para determinar possíveis correspondências. Quando o reconhecedor compara os segmentos, ele mantém uma lista de possíveis correspondências alternativas e atribui um nível de confiança a cada um, selecionando uma escolha superior.

> [!Note]  
> O reconhecedor não pode fornecer alternativas para uma parte da tinta que seja menor do que um segmento de reconhecimento.

 

 

 



