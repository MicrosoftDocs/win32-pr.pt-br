---
title: Funções e estruturas do Gerenciador de Compactação de Áudio
description: Funções e estruturas do Gerenciador de Compactação de Áudio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- áudio multimídia, funções do ACM
- áudio, funções do ACM
- gerenciador de compactação de áudio (ACM), funções
- ACM (gerenciador de compactação de áudio), funções
- áudio multimídia, estruturas do ACM
- áudio, estruturas do ACM
- gerenciador de compactação de áudio (ACM), estruturas
- ACM (gerenciador de compactação de áudio), estruturas
- Estruturas do ACM
- Funções do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd9a66bee13c02c87df95565744eb973283baedb7e955449feb2ddad3005a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808376"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funções e estruturas do Gerenciador de Compactação de Áudio

As funções do ACM se enquadram em várias categorias. As convenções de nomen entre as funções facilitam a identificação dessas categorias. Os nomes de função (com duas exceções) são do  formato *acmGroupFunction,* em que Group designa a categoria ACM (como "Driver", "Format", "FormatTag", "Filter", "FilterTag" ou "Stream") e *Função* descreve a ação executada pela função.

As funções nos grupos de filtro e formato são muito semelhantes. Quase todas as funções que atuam em filtros têm uma função paralela que atua em formatos.

No grupo de formatos, algumas funções usam marcas de formato waveform-audio (o membro **wFormatTag** de uma estrutura [**WAVEFORMATEX),**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) enquanto outras exigem formatos de áudio de forma de onda completos (a estrutura **WAVEFORMATEX** completa). (Para obter informações de referência sobre a **estrutura WAVEFORMATEX,** consulte [Erro](error.md).)

No grupo de filtros, algumas funções usam marcas de filtro waveform-audio (o **membro dwFilterTag** de uma estrutura [**WAVEFILTER),**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) enquanto outras exigem filtros de waveform-audio completos (a estrutura **WAVEFILTER** completa).

As funções no grupo de fluxo representam as várias etapas envolvidas em uma conversão: abrir uma instância de conversão, preparar para a conversão, executar a conversão, limpar após a conclusão da conversão e fechar a instância de conversão.

 

 