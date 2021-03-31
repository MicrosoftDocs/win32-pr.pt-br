---
description: Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores do modo de frase do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169725"
---
# <a name="ime-sentence-mode-values"></a>Valores do modo de frase do IME

Esses valores são usados com as funções [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| Constante                  | Definição                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| SMODE de IME \_ \_ automático     | O IME executa o processamento de conversão no modo automático.               |
| \_SMODE IME \_ nenhum          | Nenhuma informação para frase.                                               |
| \_SMODE IME \_ PHRASEPREDICT | O IME usa informações de frase para prever o próximo caractere.             |
| \_SMODE IME \_ PLURALCLAUSE  | O IME usa as informações de cláusula plural para executar o processamento de conversão. |
| \_SMODE IME \_ SINGLECONVERT | O IME executa o processamento de conversão no modo de caractere único.        |
| \_conversa de SMODE do IME \_  | O IME usa o modo de conversa. Isso é útil para aplicativos de chat.      |



 

Os bits 16 a 31 são reservados para uso do IME.

 

 



