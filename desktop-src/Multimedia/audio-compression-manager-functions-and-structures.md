---
title: Funções e estruturas do Gerenciador de compactação de áudio
description: Funções e estruturas do Gerenciador de compactação de áudio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- áudio de multimídia, funções do ACM
- áudio, funções do ACM
- Gerenciador de compactação de áudio (ACM), funções
- ACM (Gerenciador de compactação de áudio), funções
- áudio multimídia, estruturas ACM
- áudio, estruturas ACM
- Gerenciador de compactação de áudio (ACM), estruturas
- ACM (Gerenciador de compactação de áudio), estruturas
- Estruturas do ACM
- Funções do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105751624"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funções e estruturas do Gerenciador de compactação de áudio

As funções do ACM se enquadram em várias categorias. As convenções de nomenclatura para as funções facilitam a identificação dessas categorias. Os nomes de função (com duas exceções) são do formato *acmGroupFunction*, em que *Group* designa a categoria ACM (como "driver", "Format", "" FormatTag "," "Filter", "FilterTag" ou "Stream") e a *função* descreve a ação executada pela função.

As funções nos grupos de filtro e formato são muito semelhantes. Quase todas as funções que atuam em filtros têm uma função paralela que atua em formatos.

No grupo de formato, algumas funções usam marcas de formato Wave-Audio (o membro **wFormatTag** de uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ) enquanto outras exigem formatos Full Wave-Audio (a estrutura **WAVEFORMATEX** completa). (Para obter informações de referência sobre a estrutura **WAVEFORMATEX** , consulte [Error](error.md).)

No grupo de filtros, algumas funções usam marcas de filtro de onda-áudio (o membro **dwFilterTag** de uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), enquanto outras exigem filtros Full Wave-Audio (a estrutura **WAVEFILTER** completa).

As funções no grupo de fluxos representam as várias etapas envolvidas em uma conversão: abrir uma instância de conversão, preparar a conversão, executar a conversão, limpar após a conclusão da conversão e fechar a instância de conversão.

 

 