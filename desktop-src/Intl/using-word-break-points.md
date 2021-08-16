---
description: Quando o aplicativo está lidando com palavras inteiras, as posições válidas para o cursor são marcadas pelo valor do membro fWordStop da \_ estrutura LOGATTR do script. Esse valor é recuperado fazendo uma chamada para ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Usando pontos de quebra de palavras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733d761d15299e02fbfb84d541a7ceba5d4d77a9b57e0280bfeedee24532d8cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146859"
---
# <a name="using-word-break-points"></a>Usando pontos de quebra de palavras

Quando o aplicativo está lidando com palavras inteiras, as posições válidas para o cursor são marcadas pelo valor do membro **fWordStop** da estrutura [**\_ LOGATTR do script**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Esse valor é recuperado fazendo uma chamada para [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Posições válidas para linhas de quebra entre palavras são marcadas pelo valor **fSoftBreak** recuperado por [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



