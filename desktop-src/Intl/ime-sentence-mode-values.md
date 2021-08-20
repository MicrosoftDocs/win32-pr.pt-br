---
description: Revise a lista de valores de modo de frase do editor de método de entrada (IME). Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores de modo de frase do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c471282ebf50657b45f7c1c22938b27fff5a62c08c48ab4191dd84048a4b6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146125"
---
# <a name="ime-sentence-mode-values"></a>Valores de modo de frase do IME

Esses valores são usados com as [**funções ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| Constante                  | Definição                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME \_ SMODE \_ AUTOMATIC     | O IME executa o processamento de conversão no modo automático.               |
| IME \_ SMODE \_ NONE          | Nenhuma informação para frase.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | O IME usa informações de frase para prever o próximo caractere.             |
| IME \_ SMODE \_ PLURALCLAUSE  | O IME usa informações da cláusula plural para realizar o processamento de conversão. |
| IME \_ SMODE \_ SINGLECONVERT | O IME executa o processamento de conversão no modo de caractere único.        |
| IME \_ SMODE \_ CONVERSATION  | O IME usa o modo de conversa. Isso é útil para aplicativos de chat.      |



 

Os bits 16 a 31 são reservados para uso do IME.

 

 



