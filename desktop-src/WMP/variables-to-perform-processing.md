---
title: Variáveis para executar o processamento
description: Variáveis para executar o processamento
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in do eco DSP, variáveis de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636104"
---
# <a name="variables-to-perform-processing"></a>Variáveis para executar o processamento

As variáveis de membro para manipular o buffer de atraso lidam com quantidades de **bytes** ; Eles são ponteiros de **bytes** e um inteiro que armazena uma contagem de bytes. Isso é ideal para o processamento de áudio de 8 bits, uma vez que um exemplo de 8 bits se encaixa bem em um byte de memória. No entanto, ao processar o áudio de 16 bits, é mais conveniente convertê-los em ponteiros **curtos** , para que o processamento possa ocorrer dois bytes por vez.

O código de exemplo a seguir aloca os novos ponteiros de 16 bits e adiciona uma variável de ponteiro que armazena o endereço do final do buffer de atraso. Insira-o na seção "Case 16" logo antes do ponto de entrada do loop:


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



O código para o processamento de 8 bits também aloca uma variável que armazena o endereço do final do buffer de atraso. O armazenamento desse valor torna mais fácil testar se o ponteiro do buffer de atraso móvel atingiu o final do buffer de atraso. O código de exemplo a seguir calcula o valor:


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




