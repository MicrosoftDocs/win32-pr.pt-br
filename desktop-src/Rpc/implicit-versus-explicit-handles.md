---
title: Identificadores implícitos vs. explícitos
description: Para declarar um identificador de serialização, use o identificador de tipo de identificador primitivo \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823928"
---
# <a name="implicit-vs-explicit-handles"></a>Identificadores implícitos vs. explícitos

Para declarar um identificador de serialização, use o identificador de tipo de identificador primitivo [**\_ t**](/windows/desktop/Midl/handle-t). Os identificadores de serialização podem ser explícitos ou implícitos. Especifique identificadores implícitos no ACF do seu aplicativo usando o atributo de **\[ \_ identificador \] implícito** . O compilador MIDL irá gerar uma variável de identificador de serialização global. Os procedimentos de serialização com um identificador implícito usam essa variável global para acessar um contexto de serialização válido.

Ao usar a codificação de tipo, as rotinas geradas que dão suporte à serialização de um tipo específico usam o identificador implícito global para acessar o contexto de serialização. Observe que as rotinas remotas podem precisar usar o identificador implícito como um identificador de associação. Certifique-se de que o identificador implícito esteja definido como um identificador de serialização válido antes de fazer uma chamada de serialização.

Um identificador explícito é especificado como um parâmetro do protótipo de procedimento de serialização no arquivo IDL ou também pode ser especificado usando o atributo **\[ \_ identificador \] explícito** no ACF. O parâmetro identificador explícito é usado para estabelecer o contexto de serialização adequado para o procedimento. Para estabelecer o contexto correto no caso do tipo serialização, o compilador gera as rotinas de suporte que usam o parâmetro [**\_ t de identificador**](/windows/desktop/Midl/handle-t) explícito como o identificador de serialização. Você deve fornecer um identificador de serialização válido ao chamar um procedimento de serialização ou uma rotina de suporte de tipo de serialização.

 

 