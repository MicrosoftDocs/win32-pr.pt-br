---
description: Descrição de conflitos entre os gestos e caracteres e símbolos do aplicativo.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflitos entre gestos de aplicativo e caracteres e símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791256"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflitos entre gestos de aplicativo e caracteres e símbolos

Alguns gestos de aplicativo podem entrar em conflito com caracteres, combinações de caracteres, símbolos, combinações de caracteres e símbolos ou palavras inteiras escritas em um único traço. A maioria desses conflitos é evitada com uma compreensão detalhada do contexto no qual o gesto do aplicativo é executado.

Por exemplo, para distinguir um gesto direito de um traço (-) ou um sublinhado ( \_ ), um aplicativo pode filtrar por quão próximo o gesto é para os caracteres vizinhos, o tamanho relativo em comparação com os caracteres ou outras informações contidas em um pacote. O tempo do gesto do aplicativo também pode ser um fator determinante para decidir entre gestos e caracteres. Pode haver mais de uma pausa antes de aplicar um gesto de aplicativo do que antes de inserir caracteres. A menos que um usuário esteja executando uma série de gestos de desfazer ou Backspace, também pode haver mais de uma pausa após um gesto de um caractere.

Os tópicos a seguir detalham esses conflitos:

-   [Conflitos com caracteres latinos e símbolos](conflicts-with-latin-characters-and-symbols.md)
-   [Conflitos com East-Asian caracteres](conflicts-with-east-asian-characters.md)

 

 



