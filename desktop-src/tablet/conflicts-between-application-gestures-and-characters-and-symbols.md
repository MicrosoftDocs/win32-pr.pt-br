---
description: Descrição de conflitos entre gestos de aplicativo e caracteres e símbolos.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflitos entre gestos de aplicativo e caracteres e símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5819bfd7013bc39ecb622b09a1ae42816bb969ec63bf062d19597575bb958279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009016"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflitos entre gestos de aplicativo e caracteres e símbolos

Alguns gestos de aplicativo podem entrar em conflito com caracteres, combinações de caracteres, símbolos, combinações de caracteres e símbolos ou palavras inteiras escritas em um único traço. A maioria desses conflitos é evitada tendo uma compreensão detalhada do contexto no qual o gesto do aplicativo é executado.

Por exemplo, para distinguir um gesto certo de um traço (-) ou um sublinhado ( ), um aplicativo pode filtrar a proximidade do gesto com os caracteres vizinhos, o tamanho relativo em comparação com caracteres ou outras informações contidas em um \_ pacote. O tempo do gesto do aplicativo também pode ser um fator determinante na decisão entre gestos e caracteres. Pode haver mais uma pausa antes de aplicar um gesto de aplicativo do que antes de inserir caracteres. A menos que um usuário esteja executando uma série de gestos de desfazer ou de backspace, também pode haver mais uma pausa após um gesto do que um caractere.

Os tópicos a seguir detalham esses conflitos:

-   [Conflitos com símbolos e caracteres latinos](conflicts-with-latin-characters-and-symbols.md)
-   [Conflitos com caracteres East-Asian dados](conflicts-with-east-asian-characters.md)

 

 



