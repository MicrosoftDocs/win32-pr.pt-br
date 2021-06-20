---
description: Examine a lista de valores do modo de conversão do IME (editor de método de entrada). Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores do modo de conversão do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406749"
---
# <a name="ime-conversion-mode-values"></a>Valores do modo de conversão do IME

Esses valores são usados com as funções [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| bit                      | Significado                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| \_CMODE \_ alfanumérico do IME | Modo de entrada alfanumérico. Esse é o padrão, definido como 0x0000.                          |
| \_charco de CMODE IME \_     | Defina como 1 se o modo de entrada de código de caractere; 0 se não for.                                          |
| \_CMODE \_ EUDC do IME         | Defina como 1 se modo de conversão EUDC; 0 se não for.                                               |
| CMODE do IME \_ \_ corrigido        | **Windows me/98, windows 2000, Windows XP:** Defina como 1 se o modo de conversão fixa; 0 se não for. |
| \_CMODE IME \_ FULLSHAPE    | Defina como 1 se modo de forma completa; 0 se o modo de meia forma.                                        |
| \_CMODE IME \_ HANJACONVERT | Defina como 1 se o modo de conversão em HANJA; 0 se não for.                                                 |
| IME \_ CMODE \_ katakana     | Defina como 1 se modo KATAKANA; 0 se o modo HIRAGANA.                                            |
| IME \_ CMODE \_ nativo       | Defina como 1 se o modo nativo; 0 se o modo alfanumérico.                                          |
| IME \_ CMODE \_ noConversion | Defina como 1 para impedir o processamento de conversões por IME; 0 se não for.                           |
| IME \_ CMODE \_ Romano        | Defina como 1 se modo de entrada ROMAN; 0 se não for.                                                   |
| \_CMODE IME \_ SOFTKBD      | Defina como 1 se o modo de teclado virtual; 0 se não for.                                                 |
| \_símbolo de CMODE IME \_       | Defina como 1 se modo de conversão de símbolo; 0 se não for.                                             |



 

Todos os outros bits são reservados.

 

 



