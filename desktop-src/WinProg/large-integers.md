---
title: Inteiros grandes
description: As grandes funções e estruturas de inteiro forneciam originalmente suporte para valores de 64 bits em janelas de 32 bits.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- inteiros grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813996"
---
# <a name="large-integers"></a>Inteiros grandes

As grandes funções e estruturas de inteiro forneciam originalmente suporte para valores de 64 bits em janelas de 32 bits. Agora, seu compilador C pode dar suporte a inteiros de 64 bits nativamente. Por exemplo, Microsoft Visual C++ dá suporte ao tipo inteiro de tamanho [**\_ \_ Int64**](/windows/desktop/Midl/--int64) . Para obter mais informações, consulte a documentação incluída com seu compilador C.

Para obter informações sobre os inteiros de 64 bits em janelas de 64 bits, consulte [os novos tipos de dados](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Operações de inteiros grandes

Os aplicativos podem multiplicar inteiros de 32 bits assinados ou sem sinal, gerando resultados de 64 bits, usando as funções [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) e [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) . Os aplicativos podem deslocar bits em valores de 64 bits para a esquerda ou direita usando as funções [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)e [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) . Essas funções fornecem deslocamento lógico e aritmético.

Os aplicativos também podem multiplicar e dividir valores de 32 bits em uma única operação usando a função [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) . Embora o resultado da operação seja um valor de 32 bits, a função armazena o resultado intermediário como um valor de 64 bits, de modo que as informações não sejam perdidas quando valores de 32 bits grandes são multiplicados e divididos.

## <a name="large-integer-reference"></a>Referência de inteiro grande

-   [Funções de inteiro grandes](large-integer-functions.md)
-   [Estruturas de inteiro grandes](large-integer-structures.md)

 

 