---
title: Variáveis para gerenciar o buffer de atraso
description: Variáveis para gerenciar o buffer de atraso
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Plug-ins do Windows Media Player, recursos de streaming de amostra de eco
- plug-ins, amostras de eco de recursos de streaming
- plug-ins de processamento de sinal digital, Echo amostras de recursos de streaming
- Plug-ins do DSP, amostras de eco de recursos de streaming
- Exemplo de plug-in de eco do DSP, recursos de streaming
- Exemplo de plug-in do eco DSP, buffer de atraso
- buffer de atraso
- buffers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159979"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variáveis para gerenciar o buffer de atraso

Você deve adicionar as declarações para as variáveis de membro necessárias para gerenciar o buffer de atraso. Adicione as seguintes declarações a Echo. h na seção "particular":


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Adicione o seguinte código ao Construtor CEcho para inicializar as variáveis de buffer de atraso:


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




