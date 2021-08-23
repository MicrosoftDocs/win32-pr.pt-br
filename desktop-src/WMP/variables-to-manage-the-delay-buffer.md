---
title: Variáveis para gerenciar o buffer de atraso
description: Variáveis para gerenciar o buffer de atraso
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- plug-ins Windows Media Player, reproduza recursos de streaming de exemplo
- plug-ins, amostras de eco de recursos de streaming
- plug-ins de processamento de sinal digital, Echo amostras de recursos de streaming
- Plug-ins do DSP, amostras de eco de recursos de streaming
- Exemplo de plug-in de eco do DSP, recursos de streaming
- Exemplo de plug-in do eco DSP, buffer de atraso
- buffer de atraso
- buffers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571736"
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

 

 




